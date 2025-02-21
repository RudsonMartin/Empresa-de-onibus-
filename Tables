## Tabelas e Detalhes  

### Departamento  
Armazena informações sobre os departamentos da empresa.  

```sql
CREATE TABLE Departamento (
  idDepartamento INT NOT NULL AUTO_INCREMENT,
  Nome_dept VARCHAR(45) NOT NULL,
  PRIMARY KEY (idDepartamento),
  UNIQUE INDEX Nome_dept_UNIQUE (Nome_dept ASC)
) ENGINE=InnoDB;
```
- **idDepartamento**: Identificador único do departamento.  
- **Nome_dept**: Nome do departamento (Ex: RH, Operações).  

---

### Colaborador  
Gerencia informações dos colaboradores, como nome, cargo, salário e departamento.  
```sql
CREATE TABLE Colaborador (
  id_matricula INT NOT NULL AUTO_INCREMENT,
  nome VARCHAR(45) NOT NULL,
  email VARCHAR(45) NOT NULL,
  Cpf CHAR(11) NOT NULL,
  status VARCHAR(45) NOT NULL,
  salario DECIMAL(10,2) NOT NULL,
  Cargo VARCHAR(45) NOT NULL,
  Departamento_idDepartamento INT NOT NULL,
  PRIMARY KEY (id_matricula),
  UNIQUE INDEX Cpf_UNIQUE (Cpf ASC),
  UNIQUE INDEX email_UNIQUE (email ASC),
  CONSTRAINT fk_Colaborador_Departamento1
    FOREIGN KEY (Departamento_idDepartamento)
    REFERENCES Departamento (idDepartamento)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION
) ENGINE=InnoDB;
```
- **id_matricula**: Identificador único do colaborador.  
- **nome**: Nome completo do colaborador.  
- **email**: Email corporativo (único).  
- **Cpf**: Cadastro de Pessoa Física (único).  
- **status**: Situação do colaborador (ativo, inativo).  
- **salario**: Salário do colaborador.  
- **Cargo**: Cargo ocupado na empresa.  
- **Departamento_idDepartamento**: Relacionamento com a tabela **Departamento**.  

---

### Telefone_colaborador  
Armazena os números de telefone dos colaboradores.  
```sql
CREATE TABLE Telefone_colaborador (
  idTelefone INT NOT NULL AUTO_INCREMENT,
  Numero VARCHAR(45) NOT NULL,
  Colaborador_id_matricula INT NOT NULL,
  PRIMARY KEY (idTelefone),
  UNIQUE INDEX Numero_UNIQUE (Numero ASC),
  CONSTRAINT fk_Telefone_colaborador_Colaborador1
    FOREIGN KEY (Colaborador_id_matricula)
    REFERENCES Colaborador (id_matricula)
    ON DELETE NO ACTION
    ON UPDATE NO ACTION
) ENGINE=InnoDB;
```
- **idTelefone**: Identificador único do telefone.  
- **Numero**: Número de telefone.  
- **Colaborador_id_matricula**: Relacionamento com a tabela **Colaborador**.  

---

### Cidade_de_Atuação  
Registra as cidades onde a empresa opera.  
```sql
CREATE TABLE cidade_de_atuação (
  idcidade INT NOT NULL AUTO_INCREMENT,
  Nome VARCHAR(45) NOT NULL,
  PRIMARY KEY (idcidade)
) ENGINE=InnoDB;
```
- **idcidade**: Identificador da cidade.  
- **Nome**: Nome da cidade.  

---

### Status_Ônibus  
Define os possíveis status dos ônibus (Ex: Em operação, Manutenção).  
```sql
CREATE TABLE status_onibus (
  idstatus INT NOT NULL AUTO_INCREMENT,
  status VARCHAR(45) NOT NULL,
  PRIMARY KEY (idstatus)
) ENGINE=InnoDB;
```
- **idstatus**: Identificador do status.  
- **status**: Descrição do status do ônibus.  

---

### Horário_Ônibus  
Armazena os horários de operação dos ônibus.  
```sql
CREATE TABLE Horario_onibus (
  idHorario INT NOT NULL AUTO_INCREMENT,
  Horario TIME NOT NULL,
  PRIMARY KEY (idHorario),
  UNIQUE INDEX Horario_UNIQUE (Horario ASC)
) ENGINE=InnoDB;
```
- **idHorario**: Identificador do horário.  
- **Horario**: Hora de operação do ônibus.  

---

### Arrecadação_Diária  
Registra a arrecadação diária dos ônibus.  
```sql
CREATE TABLE Arrecadação_diária (
  idArrecadação INT NOT NULL AUTO_INCREMENT,
  Valor DECIMAL(10,2) NOT NULL,
  Dia DATE NOT NULL,
  PRIMARY KEY (idArrecadação)
) ENGINE=InnoDB;
```
- **idArrecadação**: Identificador da arrecadação.  
- **Valor**: Valor arrecadado no dia.  
- **Dia**: Data da arrecadação.  

---

## Observações Finais  
Este banco de dados foi projetado para garantir a integridade referencial e a consistência dos dados, utilizando **chaves primárias** e **chaves estrangeiras** em todas as tabelas.  

---
