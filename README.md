# 🤖🛡️ GuardAI: Especialista em AppSec e Análise de Vulnerabilidades

Repositório desenvolvido como parte do desafio prático do módulo [GuardAI: Agente Inteligente para Cibersegurança e Análise de Vulnerabilidades](https://web.dio.me/lab/guardai-agente-inteligente-para-ciberseguranca-e-analise-de-vulnerabilidades/learning/6304c0b9-0d50-4813-a3d9-0bed14d8670e?back=/track/bootcamp-santander-ciberseguranca-do-zero-a-pratica) da trilha de cibersegurança. Este projeto especializa o [DIO Agent](https://github.com/digitalinnovationone/dio-agent) (rodando sobre o framework Hermes) para atuar não apenas gerando código, mas conduzindo uma análise de segurança profissional — focando em contexto, impacto, probabilidade, severidade e mitigação.

---

## 🎯 A Especialização do Agente e o Porquê
O agente foi treinado exclusivamente via arquivos de configuração, conhecimento e *skills* (sem treino de modelos) para adotar uma postura defensiva orientada a processos. 
* **Por quê?** Em cibersegurança, sugerir comandos de correção ou exploração sem entender o ambiente do usuário (como versão de sistemas, exposição na rede ou criticidade dos dados) pode causar graves incidentes. O GuardAI agora prioriza **perguntar o contexto** antes de agir.

---

## 📁 Arquivos Criados e Alterados
Para estruturar essa especialização, os seguintes componentes foram implementados no repositório base:

1. **Nova Skill (`skills/vulnerability-analysis/`)**
   - `SKILL.md`: Roteiro passo a passo com regras defensivas para o agente seguir durante a varredura de falhas (como SQL Injection e análise de código inseguro).
   - `README.md`: Documentação explicativa da skill para humanos.
2. **Base de Conhecimento (`agent/knowledge/security-basics.md`)**
   - Inserção de conceitos fundamentais como vulnerabilidade, ameaça, risco, a Tríade CIA (Confidencialidade, Integridade e Disponibilidade) e boas práticas de desenvolvimento seguro.
3. **Ajuste de Persona (`agent/persona.md`)**
   - Incorporação do tom profissional de um especialista em AppSec e mentor de segurança.
4. **Registro de Habilidades (`AGENTS.md`)**
   - Adição da linha correspondente na tabela de skills para garantir que o agente saiba quando acionar a nova habilidade de análise.

---

## 🚀 Como Rodar o Agente no Hermes
> ⚠️ **Atenção:** Certifique-se de abrir o terminal diretamente na pasta raiz do projeto clonado para que o Hermes consiga ler os diretórios de configuração.

1. Clone o repositório oficial base [dio-agent](https://github.com/digitalinnovationone/dio-agent) ou utilize a sua versão evoluída:
   ```bash
   git clone [https://github.com/seu-usuario/nome-do-repositorio.git](https://github.com/seu-usuario/nome-do-repositorio.git)
   cd nome-do-repositorio

   Siga as instruções de instalação do framework Hermes descritas no README original do projeto.

Inicie o harness/terminal do agente na raiz da pasta e teste a análise criando um arquivo de exemplo app.py vulnerável a SQL Injection para validar as perguntas de contexto do assistente.

📈 Melhoria Escolhida (Evolução)
Padronização de Relatórios de Severidade: Além da estrutura padrão, a skill foi aprimorada para forçar a saída de análise sempre estruturada em formato de Impacto, Probabilidade e Severidade, facilitando a priorização de correção no fluxo de DevSecOps.

Desenvolvido por N13 durante a jornada do bootcamp de cibersegurança.
