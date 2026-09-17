CREATE TABLE DISCIPLINA (
    CODIGO_DISCIPLINA VARCHAR2(5) PRIMARY KEY,
    DESCRICAO VARCHAR(50) NOT NULL
);

CREATE TABLE PROFESSOR (
    CODIGO NUMBER PRIMARY KEY,
    NOME VARCHAR2(100) NOT NULL,
    CODIGO_DISCIPLINA VARCHAR2(5),
    CONSTRAINT FK_PROFESSOR_DISCIPLINA FOREIGN KEY (CODIGO_DISCIPLINA)
        REFERENCES DISCIPLINA (CODIGO_DISCIPLINA)
);

CREATE TABLE TURMA (
    CODIGO VARCHAR2(10) PRIMARY KEY,
    NOME_TURMA VARCHAR2(60) NOT NULL
);

CREATE TABLE ALUNO (
    CODIGO NUMBER PRIMARY KEY,
    NOME VARCHAR2(100) NOT NULL,
    IDADE NUMBER(2) NOT NULL,
    TURMA VARCHAR2(10) NOT NULL,
    CONSTRAINT FK_ALUNO_TURMA FOREIGN KEY (TURMA)
        REFERENCES TURMA (CODIGO)
);
INSERT INTO DISCIPLINA (codigo_disciplina, descricao)
VALUES ('BD', 'BANCO DE DADOS');

INSERT INTO DISCIPLINA (codigo_disciplina, descricao)
VALUES ('EN', 'INGLÊS');

INSERT INTO PROFESSOR (codigo, nome, codigo_disciplina)
VALUES (1, 'Charles Caleiro', 'BD');

INSERT INTO PROFESSOR (codigo, nome, codigo_disciplina)
VALUES (2, 'Tiago Vieira', 'EN');

INSERT INTO TURMA (codigo, nome_turma) VALUES ('701MAT', 'Sétima Série Um Matutino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('702MAT', 'Sétima Série Dois Matutino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('801MAT', 'Oitava Série Um Matutino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('802VES', 'Oitava Série Dois Vespertino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('901MAT', 'Nona Série Um Matutino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('902VES', 'Nona Série Dois Vespertino');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('101INFO', 'Primeiro Ano Um Técnico em Informática');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('102LOG', 'Primeiro Ano Dois Técnico em Logística');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('104LOG', 'Primeiro Ano Quatro Técnico em Logística');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('106INFO', 'Primeiro Ano Seis Técnico em Informática');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('201SST', 'Segundo Ano Um Técnico em Segurança do Trabalho');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('201EDF', 'Segundo Ano Um Técnico em Edificações');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('202INFO', 'Segundo Ano Dois Técnico em Informática');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('301POR', 'Terceiro Ano Um Técnico em Portos');
INSERT INTO TURMA (codigo, nome_turma) VALUES ('302EDF', 'Terceiro Ano Dois Técnico Em Edificação');

INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (1, 'Gabriel Souza', 13, '701MAT');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (2, 'Ana Beatriz Lima', 13, '702MAT');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (3, 'Lucas Oliveira', 14, '801MAT');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (4, 'Maria Eduarda Santos', 14, '802VES');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (5, 'Pedro Henrique Costa', 15, '901MAT');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (6, 'Isabela Ferreira', 15, '902VES');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (7, 'Matheus Almeida', 15, '101INFO');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (8, 'Sophia Rodrigues', 16, '102LOG');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (9, 'Guilherme Pereira', 16, '104LOG');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (10, 'Laura Martins', 16, '106INFO');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (11, 'Rafael Carvalho', 16, '201SST');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (12, 'Julia Gomes', 17, '201EDF');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (13, 'Bruno Ribeiro', 17, '202INFO');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (14, 'Beatriz Barbosa', 17, '301POR');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (15, 'Enzo Araújo', 18, '302EDF');
INSERT INTO ALUNO (codigo, nome, idade, turma) VALUES (16, 'Manuela Dias', 13, '701MAT');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (17, 'Miguel Nascimento', 13, '702MAT');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (18, 'Alice Monteiro', 14, '801MAT');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (19, 'Davi Cardoso', 14, '802VES');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (20, 'Valentina Teixeira', 15, '901MAT');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (21, 'Arthur Correia', 15, '902VES');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (22, 'Lorena Pinto', 15, '101INFO');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (23, 'Heitor Moreira', 16, '102LOG');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (24, 'Yasmin Cavalcante', 16, '104LOG');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (25, 'Theo Rocha', 16, '106INFO');
INSERT INTO aluno (codigo, nome, idade, turma) VALUES (26, 'Helena Batista', 16, '201SST');
