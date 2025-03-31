# System Monitoring Tool

<img width="222" alt="system_monitor_hyper_logo" src="https://github.com/user-attachments/assets/3a2eb494-9951-4c0e-80f2-a34fe1d5c2ff" />


Uma ferramenta avançada de monitoramento de sistema que fornece informações detalhadas sobre o uso de recursos do computador, com interface gráfica (GUI).

## 📌 Visão Geral

Este script monitora em tempo real:
- Uso de CPU (por núcleo e agregado)
- Memória RAM e Swap
- Utilização de disco
- Atividade de rede
- Processos em execução

Gera relatórios HTML estilizados com Bootstrap e gráficos interativos.

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- Bibliotecas principais:
  - `psutil` - Coleta de métricas do sistema
  - `tkinter` - Interface gráfica
  - `matplotlib` - Visualização de dados
  - `Bootstrap` (HTML) - Relatórios formatados

## 🏗️ Estrutura do Código

### 📦 Importações Principais
```python
import psutil
import platform
import tkinter as tk
from tkinter import ttk, messagebox
import matplotlib.pyplot as plt
import argparse

⚙️ Configuração
Arquivo config.json armazena preferências do usuário

Valores padrão incluídos para primeira execução

🚨 Sistema de Alertas
Monitora condições críticas:

Vazamentos de memória

Uso excessivo de CPU

Consumo alto de memória

Swap utilization

📊 Classe Principal - SystemMonitor
python
Copy
class SystemMonitor:
    def __init__(self):
        self.config = self.load_config()
        self.alert_manager = AlertManager()
        
    def get_system_info(self):
        """Coleta informações abrangentes do sistema"""
        # Implementação...
    
    def monitor_system(self):
        """Loop principal de monitoramento"""
        # Implementação...

🖥️ Interface Gráfica - SystemMonitorGUI
python
Copy
class SystemMonitorGUI:
    def __init__(self):
        self.root = tk.Tk()
        self.setup_gui()
        
    def setup_gui(self):
        """Configura todos os elementos da interface"""
        # Implementação...

🚀 Funcionalidades
Monitoramento em Tempo Real
Gráficos dinâmicos de uso de recursos

# Ferramenta de Monitoramento de Sistema

Uma ferramenta completa de monitoramento de recursos do sistema com suporte a interface gráfica (GUI) e linha de comando (CLI), relatórios detalhados e capacidades de alerta.

## 📖 Visão Geral
Este script fornece informações detalhadas sobre o uso de recursos do computador através de uma interface gráfica (GUI) e linha de comando (CLI). Monitora:
- Uso da CPU
- Consumo de memória
- Atividade do disco
- Tráfego de rede
- Processos em execução

Gera relatórios HTML estilizados com Bootstrap e inclui alertas em tempo real para limites de recursos.

## 🧠 Estrutura do Código

### 📦 Importações
- Monitoramento: `psutil`, `platform`, `os`, `datetime`
- Componentes GUI: `tkinter`, `matplotlib`
- Processamento de dados: `collections`, `argparse`, `csv`, `json`
- Recursos avançados: `logging`, `tracemalloc`, `ctypes`

### ⚙️ Configuração
```python
CONFIG_FILE = "config.json"
DEFAULT_CONFIG = {
    "monitor_interval": 2,
    "max_duration": 600,
    # ... outros padrões
}
Criação automática do arquivo de configuração

Tratamento de erros no carregamento

🚨 Gerenciador de Alertas
Histórico com collections.deque

Disparo inteligente baseado em médias históricas

Prevenção de alertas duplicados

🔍 Classe SystemMonitor
Principais Métodos:

get_system_info(): Snapshot completo do hardware/SO

get_processes_info(): Agregação de métricas de processos

check_memory_leak(): Análise de alocação de memória

generate_report(): Geração de relatórios HTML/CSV

🖥️ Implementação GUI
Recursos:

Interface com temas (Claro/Escuro/Azul)

Dashboard de métricas em tempo real

Visualização em árvore de processos

Gráficos interativos

Gerenciamento de configurações

🛠️ Funcionalidades
🖱️ Modo GUI
bash
Copy
python monitor.py --gui
Aba de configuração para ajustes

Monitoramento em tempo real

Testes de estresse integrados

Personalização de temas

⌨️ Modo CLI
bash
Copy
python monitor.py --interval 5 --duration 300 --output relatorio.html
Monitoramento não interativo

Amostragem programada de recursos

Geração automática de relatórios

🌟 Recursos Principais
Monitoramento multi-thread

Suporte multiplataforma (Windows/macOS/Linux)

Relatórios HTML com Bootstrap

Visualização de dados com Matplotlib

Detecção de vazamento de memória

Limites de alerta configuráveis

Acompanhamento de processos específicos

Interface GUI temática

Tratamento abrangente de exceções

📈 Exemplo de Relatório
Inclui:

Tabela resumo do sistema

Linha do tempo de uso de recursos

Gráficos de principais processos

Histórico de alertas

Detalhes de hardware

Exportação para CSV

🔮 Melhorias Potenciais
python
Copy
# Área de melhoria exemplo
def optimizar_desempenho():
    implementar_cache()
    adicionar_otimizacoes_especificas()
    melhorar_gerenciamento_memoria()
Desempenho

Análise de uso de recursos

Coleta assíncrona de dados

Recursos

Monitoramento de portas de rede

Suporte a containers Docker

Integração com nuvem

Segurança

Criptografia de arquivos de configuração

Autenticação de usuário

Usabilidade

Relatórios responsivos

Exportação para PDF/Excel

Sistema de notificações

🚀 Começando
Requisitos
bash
Copy
pip install -r requirements.txt
Python 3.8+

psutil

matplotlib

Pillow

tqdm

Instalação
Clone o repositório:

bash
Copy
git clone https://github.com/seu-usuario/system-monitor.git
cd system-monitor
Instale as dependências:

bash
Copy
pip install -r requirements.txt
Uso Básico
Interface Gráfica:

bash
Copy
python monitor.py --gui
Linha de Comando:

bash
Copy
python monitor.py --interval 5 --duration 60 --output meurelatório.html
Como módulo:

python
Copy
from system_monitor import SystemMonitor

monitor = SystemMonitor()
dados_sistema = monitor.get_system_info()
