# Getting Started  
In this chapter, let's build the TEN Agent playground together.  

## Prerequisites  
**API Keys**  
- Agora [App ID](https://docs.agora.io/en/video-calling/get-started/manage-agora-account?platform=web#create-an-agora-project) and [App Certificate](https://docs.agora.io/en/video-calling/get-started/manage-agora-account?platform=web#create-an-agora-project) (free minutes every month)  

**Installations**  
- [Docker](https://www.docker.com/) / [Docker Compose](https://docs.docker.com/compose/)  
- [Node.js(LTS) v18](https://nodejs.org/en)  

**Minimum system requirements**  
- CPU >= 2 Core  
- RAM >= 4 GB  

**Docker setting on Apple Silicon**  
For Apple Silicon Macs, uncheck "Use Rosetta for x86/amd64 emulation" in Docker settings. Note: This may result in slower build times on ARM, but performance will be normal when deployed to x64 servers.  

## Next step  
**1. Clone down the TEN Agent repository**  
```bash  
git clone https://github.com/TEN-framework/TEN-Agent.git  
```  

**2. Prepare config files**  
```bash  
cp ./.env.example ./.env  
```  

**3. Setup Agora App ID and App Certificate in .env file**  
```env  
AGORA_APP_ID=  
AGORA_APP_CERTIFICATE=  
```  

**4. Start agent builder toolkit containers**  
```bash  
docker compose up -d  
```  

**5. Enter container**  
```bash  
docker exec -it ten_agent_dev bash  
```  

**6. Build the agent**  
```bash  
task use  
```  

**7. Start the web server**  
```bash  
task run  
```  

**8. Edit playground settings**  
Open the playground at [localhost:3000](http://localhost:3000) to configure your agent:  
1. Select a graph type (e.g. Voice Agent, Realtime Agent)  
2. Choose a corresponding module  
3. Select an extension and configure its API key settings