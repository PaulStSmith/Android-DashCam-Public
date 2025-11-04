# DashCam v1.0.0 Notas da Versão

## Visão Geral

DashCam v1.0.0 é a versão inicial de uma aplicação avançada de dashcam que transforma telemóveis Android antigos em câmaras de veículo profissionais. Esta versão introduz capacidades abrangentes de gravação de vídeo, deteção de impacto, telemetria GPS e funcionalidades de carregamento na nuvem utilizando tecnologias Android modernas.

## Principais Funcionalidades

### 🎥 Funcionalidades de Gravação Core
- **Integração CameraX**: Gravação de vídeo de alta qualidade com codificação acelerada por hardware
- **Telemetria em Tempo Real**: Dados de localização GPS, velocidade e direção incorporados como legendas SRT
- **Múltiplos Modos de Gravação**:
  - **Modo AUTO**: Gravação de buffer circular com deteção inteligente de impacto que guarda automaticamente sequências críticas durante colisões
  - **Modo Por Viagem**: Início/paragem automática de gravação baseada na ligação de energia do veículo
  - **Modo Loop Temporizado**: Segmentos configuráveis de 5/10/30 minutos com gestão transparente de ficheiros

### 🚗 Deteção de Impacto & Segurança
- **Deteção Baseada em Acelerómetro**: Algoritmos avançados detetam impactos repentinos e protegem sequências importantes
- **Buffer Circular**: Gravação contínua com limpeza automática enquanto preserva momentos críticos
- **Proteção de Ficheiros**: Gravações importantes são automaticamente marcadas e protegidas contra eliminação

### ☁️ Sistema de Carregamento na Nuvem
- **Suporte Multi-Plataforma**: Carregamento para Google Drive, OneDrive e partilhas de rede SMB/CIFS
- **Processamento em Segundo Plano**: Worker de carregamento fiável que continua mesmo quando a app está fechada
- **Gestão de Rede**: Políticas de carregamento configuráveis apenas WiFi ou rede medida
- **Gestão de Fila**: Visualizador visual de fila de carregamento com funcionalidade de repetição e rastreamento de progresso
- **Integração OAuth**: Autenticação segura para serviços na nuvem

### ⚙️ Definições Avançadas
- **Configuração Abrangente**: Unidades de velocidade (mph/km/h), formatos de data/hora, definições de qualidade de vídeo
- **Gestão de Armazenamento**: Caminhos de armazenamento personalizados, limpeza automática e organização de ficheiros
- **Gestão de Energia**: Manipulação de otimização de bateria e controlos de tempo limite de ecrã
- **Relatórios de Falha**: Integração opcional do Firebase Crashlytics para diagnósticos

### 🎨 Interface de Utilizador Moderna
- **Jetpack Compose**: UI moderna e declarativa com animações suaves
- **Material Design 3**: Linguagem de design consistente com suporte de tema escuro/claro
- **Experiência Imersiva**: Vista de câmara em ecrã completo com barras do sistema ocultas
- **Suporte Multi-Idioma**: Interface localizada em múltiplos idiomas

### 🔧 Funcionalidades Técnicas
- **Serviço em Primeiro Plano**: Funcionamento fiável em segundo plano para gravação contínua
- **Integração WorkManager**: Carregamentos programados em segundo plano e tarefas de manutenção
- **Preferências DataStore**: Armazenamento seguro e eficiente de definições
- **Manipulação de Permissões**: Gestão abrangente de permissões para câmara, localização e armazenamento
- **Otimização de Bateria**: Manipulação inteligente das restrições de bateria do Android

## Requisitos do Sistema
- **Versão do Android**: 8.0 (API 26) ou superior
- **Hardware**: Câmara, GPS, sensores de acelerómetro
- **Armazenamento**: Espaço suficiente para gravações de vídeo e buffer circular

## Limitações Conhecidas
- Requer dispositivo Android com capacidades adequadas de câmara e sensores
- Carregamento na nuvem requer ligação estável à internet
- Algumas funcionalidades podem ter funcionalidade limitada em versões mais antigas do Android

## Instalação
Instale o ficheiro APK num dispositivo Android compatível. Conceda todas as permissões solicitadas para funcionalidade completa.

## Suporte
Para problemas, pedidos de funcionalidades ou perguntas, consulte a documentação do projeto ou contacte a equipa de desenvolvimento.

## Planos Futuros
- Integração de monitorização de temperatura
- Funcionalidade aprimorada de backup na nuvem
- Temas adicionais de UI e opções de personalização
- Suporte expandido de plataforma

---

*Lançado: 3 de novembro de 2025*  
*Versão: 1.0.0 (Build 1)*</content>
<parameter name="filePath">c:\Users\pauls\source\repos\DashCam\public\lang\pt-rPT\release-notes-v1.md