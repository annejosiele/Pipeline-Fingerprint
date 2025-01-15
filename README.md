# Pipeline-Fingerprint

## Descrição do Projeto
Este pipeline gera descritores moleculares (fingerprints) a partir de SMILES canônicos utilizando o algoritmo Morgan (baseado em Tanimoto). Ele processa os dados químicos fornecidos, remove duplicatas e cria um conjunto de dados contendo os fingerprints moleculares associados aos compostos identificados.

## Requisitos
As bibliotecas necessárias para executar o pipeline são:

- Python 3.8 ou superior
- pandas
- rdkit

Para instalar todas as dependências, execute o seguinte comando:
```bash
pip install pandas rdkit
```

## Instruções de Uso
1. Certifique-se de que o arquivo de dados de entrada no formato Excel (.xlsx) contém as colunas Chemical-Name e row-with-SMILES.
2. Substitua o caminho do arquivo na linha:
```python
df = pd.read_excel("your-dataset-with-SMILES-descriptors.xlsx")
```
pelo caminho do seu arquivo de dados.
3. Execute o script para gerar um conjunto de dados Excel contendo os fingerprints moleculares para cada composto químico identificado.
4. O arquivo final será salvo como Name-Your-Dataset-With-Fingerprints.xlsx na mesma pasta do script.

## Estrutura do Repositório
Sugerimos que a estrutura do repositório seja organizada da seguinte forma:

```python
root/
├── data/
│   └── your-dataset-with-SMILES-descriptors.xlsx  # Conjunto de dados de entrada
├── output/
│   └── Name-Your-Dataset-With-Fingerprints.xlsx   # Conjunto de dados final com fingerprints
├── src/
│   └── pipeline_fingerprint.py                    # Script principal do pipeline
├── README.md                                      # Documentação do projeto
└── requirements.txt                               # Lista de dependências do projeto
```

## Licença
Este projeto está licenciado sob a licença MIT. Consulte o arquivo `LICENSE` para obter mais detalhes.

## Contribuições
Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request.
