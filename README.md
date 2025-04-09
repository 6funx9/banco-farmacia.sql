CREATE TABLE Farmacia ( 
    idFarmacia INT PRIMARY KEY,  
    nome_farmacia VARCHAR(100),  
    end_farmacia VARCHAR(255),  
    Tel_farmacia VARCHAR(20),  
    CNPJ_farmacia VARCHAR(20)  
);

CREATE TABLE Produto ( 
    cod_produto INT PRIMARY KEY,  
    qtd_produto INT,  
    valor_produto DECIMAL(10, 2),  
    idFarmacia INT,  
    FOREIGN KEY (idFarmacia) REFERENCES Farmacia (idFarmacia)
);

CREATE TABLE Farmaceutico ( 
    RG_farmaceutico VARCHAR(20) PRIMARY KEY,  
    nome_farmaceutico VARCHAR(100),  
    idFarmacia INT,  
    FOREIGN KEY (idFarmacia) REFERENCES Farmacia (idFarmacia)
);
