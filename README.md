## Teste SRE
Este repositório contém ferramentas de automação e infraestrutura para testar habilidades de SRE (Site Reliability Engineering), com foco no deployment do Apache Airflow e no gerenciamento de incidentes.

## Visão Geral do Projeto
Este projeto fornece uma configuração baseada em Docker para implantar o Apache Airflow, juntamente com um conjunto de scripts e configurações para simular e gerenciar cenários operacionais. Ele inclui:

- Implantação Airflow via docker-compose.yaml
- Documentação de Incidente (PostMortem)
- Decritivo de Ações

## Serviços Incluídos
O arquivo compose.yaml cria os seguintes serviços:

**Postgres**: Banco de dados para os metadados do airflow
**Redis**: Serviço de mensageria para as filas de execuções
**Airflow Webserver**: Interface WEB do Airflow
**Airflow Scheduler**: Agendador de DAG
**Airflow Worker**: Container que executa as tarefas
**Flower**: Interface WEB que monitora as tarefas do Celery

## Executar
Para colocar o ambiente em execução, rode o comando:
docker compose --profile flower up --force-recreate --always-recreate-deps -d --remove-orphans

**Os parâmetros --force-recreate, --always-recreate-deps e --remove-orphans não são necessários.**
