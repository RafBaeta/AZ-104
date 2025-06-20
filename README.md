# AZ-104
DIO.me Labs

Configuração de Máquinas Virtuais no Azure
Objetivos
Compreender os modelos de responsabilidade em serviços de nuvem (SaaS, PaaS, IaaS)

Planejar e configurar uma máquina virtual

Conectar a VMs Windows e Linux

Configurar a disponibilidade da máquina virtual no Azure

Matriz de Responsabilidade em Serviços de Nuvem
Tipo	Gerenciado pelo Cliente	Gerenciado pela Microsoft
On-Premises	Tudo (rede, hardware, SO, dados, etc.)

IaaS (Infraestrutura como Serviço)	SO, middleware, dados, aplicativos	Hardware, rede, virtualização
PaaS (Plataforma como Serviço)	Dados e lógica de aplicativos	Infraestrutura, SO, runtime
SaaS (Software como Serviço)	Uso e configuração do app	Todo o restante (infra, app)

SaaS: Ex: Microsoft 365

PaaS: Ex: Azure SQL Database

IaaS: Ex: Máquinas virtuais no Azure

Planejamento de Máquina Virtual
1. Rede
Comece pela criação da VNet e Subnet.

2. Nome da VM
Use nomes padronizados e descritivos.

3. Região
Escolha baseada em proximidade dos usuários e requisitos legais.

Os preços variam por região.

Dimensionamento da VM
Uso Geral: Equilíbrio entre CPU e RAM.

Computação Otimizada: Mais CPU, para tarefas intensivas (ex: cálculos).

Memória Otimizada: Mais RAM, ideal para bancos de dados.

GPU: Para renderização gráfica, IA, edição de vídeo.

Computação de Alto Desempenho (HPC): Máxima performance de CPU.

Armazenamento da VM
Cada VM pode ter:

Disco do SO: (Ex: C:\)

Disco Temporário: (D:\) – pode ser apagado!

Discos de Dados: Opcional, para armazenamento adicional.

Os discos estão em contas de armazenamento gerenciadas.

Acesso Seguro
Azure Bastion: Acesso via browser (RDP/SSH) sem expor IP público.

SSH: Recomendado uso de chaves privadas com senha para VMs Linux.

Alta Disponibilidade de VMs no Azure
1. Manutenção de Hardware Não Planejada
O Azure pode prever falhas e mover VMs com migração em tempo real (sem downtime).

2. Manutenção Planejada
Atualizações agendadas da plataforma, geralmente sem impacto direto.

Conjuntos de Disponibilidade (Availability Sets)
Evita que múltiplas VMs sejam afetadas por uma falha única.

Domínio de Falha (Fault Domain): Racks físicos.

As VMs são distribuídas para evitar falhas de hardware simultâneas.

Domínio de Atualização (Update Domain): Ciclos de atualização.

Permite atualizações de sistema sem derrubar todas as VMs.

Escalabilidade: Vertical vs. Horizontal
Escala Vertical (Up/Down)
Aumenta ou reduz recursos de uma única VM (CPU, RAM, disco).

Escala Horizontal (Out/In)
Aumenta ou reduz o número de VMs com base em demanda (ex: Black Friday).

Clona VMs com base em uso, de forma automatizada.

Dimensionamento Automático (Auto Scale)
Defina:

Número mínimo e máximo de VMs

Percentual de uso de CPU para escalar

Análise padrão: 10 minutos

Exemplo:

Se CPU > 70% por 10min → adiciona uma VM.
Se CPU < 30% por 10min → remove uma VM."


