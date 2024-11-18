# 🚀 Stack MySQL + Grafana + Prometheus  

Este repositório contém os arquivos necessários para subir uma stack com MySQL, Grafana e Prometheus. Abaixo estão as instruções para configuração e uso.  

---

## 🛠️ Como executar a stack  

### 1. Subir a stack  
Execute o comando abaixo para iniciar os serviços:  
```bash  
docker compose up -d  
```  

### 2. Configurar o MySQL  
1. Entre no container do MySQL:  
   ```bash  
   docker container exec -it mysql /bin/bash  
   ```  
2. Acesse o MySQL com o usuário root:  
   ```bash  
   mysql -u root -p -h 127.0.0.1  
   ```  
   **Senha do root:** `123456` (definida no arquivo `compose.yml`).  

3. Crie o usuário conforme especificado no `compose.yml`:  
   ```sql  
   CREATE USER 'msqluser'@'%' IDENTIFIED BY 'msqlpassword' WITH MAX_USER_CONNECTIONS 3;  
   GRANT PROCESS, REPLICATION CLIENT, SELECT ON *.* TO 'msqluser'@'%';  
   ```  

4. Saia do MySQL e do container:  
   ```bash  
   exit  
   exit  
   ```  

---

## 🌟 Configurar o Grafana  

### 1. Acessar o Grafana  
1. Abra o navegador e vá para: [http://localhost:3000](http://localhost:3000).  
2. Faça login com as credenciais:  
   - **Usuário:** `admin`  
   - **Senha:** `admin`  

### 2. Configurar o Data Source Prometheus  
1. Navegue até **Connections > Add new datasource > Prometheus**.  
2. Adicione um novo Data Source com as seguintes configurações:  
   - **Tipo:** Prometheus  
   - **Prometheus server URL:** `http://prometheus:9090`  

### 3. Importar o Dashboard  
1. Vá até **Dashboards > New > Import**.  
2. Insira o **ID do Dashboard**: `14057`.  
3. Confirme a importação e selecione o Data Source configurado anteriormente.  

---

## 🎉 Pronto!