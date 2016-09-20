##1
SELECT * FROM Impressoras;
##2
SELECT pessoas.id,pessoas.nome,cargo.* ,funcionarios.* FROM pessoas,cargo,funcionarios
WHERE funcionarios.pessoas_id = pessoas.id AND funcionarios.cargo_id = cargo_id;
##3
SELECT endereco.cidade FROM endereco
GROUP BY endereco.cidade;
##4
SELECT * FROM atendimento
JOIN Impressoras ON atendimento.impressoras.id = Impressoras.id
JOIN pessoas ON pessoas.id = clientes.pessoas_id AND atendimento.clientes_id = clientes_id
JOIN endereco ON pessoas.id = endereco.id;
##5
SELECT atendimento.data FROM atendimento
WHERE DATE(atendimento.data) = "%12/2015%"
JOIN pessoas.nome ON pessoas.id = clientes.pessoas_id AND atendimento.clientes_id = clientes.id;
##6
SELECT * FROM funcionarios
JOIN AVG(cargo.salario) ON cargo.id = funcionarios.cargo_id;
##7
SELECT * FROM atendimento
GROUP BY atendimento.impressoras_id
JOIN SUM(atendimento.num_paginas) ON atendimento.impressoras_id = impressoras.id;
##8
SELECT atendimento.data FROM atendimento
JOIN SUM(atendimento.valor)
GROUP BY YEAR(atendimento.data)
ORDER BY YEAR(atendimento.data);
##9
SELECT atendimento.data FROM atendimento
JOIN SUM(atendimento.valor)
GROUP BY MONTH(atendimento.data)
ORDER BY MONTH(atendimento.data);
##10

##11

##12
