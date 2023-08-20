# Case 4
Na Dadosfera, temos uma base de dados com informações fictícias de uma empresa. Foi
demandado pela sua liderança de CS, que você crie análises descritivas da própria área com base nesses dados.
Você pode ver mais detalhes aqui neste link. Utilize as mesmas credenciais para acessar nosso módulo de Visualização. Observe que você precisa utilizar o identificador da tabela para encontrá-la no nosso módulo de Visualização:
Crie uma Coleção com o formato <nome> <sobrenome> - <mes_ano> assim como no
exemplo:
Crie uma visualização de dados como estas abaixo. Salve a Query SQL utilizada e também o print do resultado da query no documento markdown deste teste.

Abaixo estarão as querys utilizadas, bem como os links das imagens dos resultados obtidos e as visualizações de dados:

- Query utilizada para realizar a visualização de dados dos cargos:

SELECT
CASE
        WHEN jobrole IN ('Sales Executive', 
        'Research Scientist', 
        'Laboratory Technician', 
        'Manufacturing Director', 
        'Healthcare Representative') 
        THEN jobrole
        ELSE 'Outros Cargos'
    END AS cargos,
    COUNT(*) AS total_empregados
FROM TB__TAEZZB__EMPLOYEE
GROUP BY cargos;

Resultado da query - https://ibb.co/6FVS86r
Visualização dos dados - https://ibb.co/DCSJJbD


- Query utilizada para visualização de dados do departmento

SELECT department, COUNT(*) AS total_empregados
FROM TB__TAEZZB__EMPLOYEE
WHERE department IN ('Human Resources', 'Research & Development', 'Sales') 
GROUP BY department;

Resultado da query - https://ibb.co/HTvzpwL
Visualização dos dados - https://ibb.co/kGgdKgL


