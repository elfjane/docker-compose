
You: 

docker-compose apache airflow

ChatGPT: 

�A�Q�� Docker Compose �ӳ��p Apache Airflow �ܡH�٬O�A���S�w���ݨD�A�Ҧp�ۭq�]�w�B�s�� MySQL/MariaDB�A�ξ�X��L�A�ȡH
�p�G�u�O�n�ֳt�Ұ� Apache Airflow�A�x�责�ѤF�@�Ӳ{���� `docker-compose.yaml`�A�i�H�o�ˤU���ð���G
### 1. �U���x��d�� 


```bash
curl -LfO 'https://airflow.apache.org/docs/apache-airflow/stable/docker-compose.yaml'
```
2. �إ� `.env` �]�w��

```bash
echo -e "AIRFLOW_UID=$(id -u)" > .env
```

### 3. ��l�� Airflow 


```bash
docker-compose up airflow-init
```

### 4. �ҰʪA�� 


```bash
docker-compose up -d
```

�o�|�ҰʡG
 
- `airflow-webserver`�]UI �ɭ��^
 
- `airflow-scheduler`�]�Ƶ{���^
 
- `airflow-worker`�]������ȡ^
 
- `airflow-init`�]��l�Ƹ�Ʈw�^
 
- `postgres`�]Airflow �w�]�� metadata DB�^

### 5. �n�J Airflow 
 
- �w�]�޲z���b���G

```makefile
username: airflow
password: airflow
```
 
- UI �J�f�G

```arduino
http://localhost:8080
```

�p�G�A���ݨD��������A�Ҧp�G
 
- **��� MySQL/MariaDB �Ӥ��O PostgreSQL**
 
- **��X Apache�BNginx �N�z**
 
- **�X�i Worker �`�I**
�i�H�A�`�J�վ� `docker-compose.yaml`�C�A���S�w�ݨD�ܡH
