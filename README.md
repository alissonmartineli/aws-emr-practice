# Prática com AWS EMR e Python

## Bucket S3

Acessar o S3, criar um bucket com a seguinte estrutura de pastas e realizar o upload do arquivo _sherlock.txt_ para a data temp:

```
|_ data/
|  |_ sherlock.txt
|_ output/
|_ temp/
```

## Chave SSH

Acessar o serviço EC2, criar uma par de chaves e realizar o download do arquivo .pem.

## Chaves de acesso

Acessar **My Security Credentials**, criar uma nova chave de acesso e realizar o download do arquivo.

## Dependências

```
pip install -r requirements.txt
```

## Configurações

Preencher o arquivo _mrjob.conf_ com as credenciais geradas e região correta.

## Execução

Configurar com o nome do bucket criado e executar o job.

```
python3 word_freq_count.py -r emr s3://<NOME_DO_SEU_BUCKET>/data/sherlock.txt --output-dir=s3://<NOME_DO_SEU_BUCKET>/output/logs --cloud-tmp-dir=s3://<NOME_DO_SEU_BUCKET>/temp/ -c mrjob.conf
```
