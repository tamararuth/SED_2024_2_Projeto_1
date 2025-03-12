# Controle de Robôs Autônomos em um Armazém

Este repositório contém a documentação do projeto de controle supervisionado para um sistema de robôs móveis em um armazém utilizando **autômatos finitos** e a ferramenta **Supremica**.

## Descrição Geral

O projeto modela e controla um sistema onde **três robôs autônomos** transportam caixas de insumos entre um **Buffer de Entrada (BE)** e **quatro máquinas de processamento (M1, M2, M3, M4)**. O Supremica é utilizado para sintetizar um supervisor que garante a **operação segura e eficiente** dos robôs.

## Objetivos

### Modelar o sistema de transporte de insumos
- Representar o comportamento dos robôs usando autômatos finitos.
- Definir estados e transições para o transporte de caixas entre o **BE** e as máquinas.
- Garantir que o robô tem acesso ao BE.

### Implementar a especificação e gerar o supervisor
- Modelar restrições de segurança usando autômatos de especificação.
- Utilizar o **Supremica** para a síntese do supervisor.

### Simular e validar o comportamento do sistema
- Testar cenários de transporte para verificar a segurança do supervisor.
- Avaliar a performance do sistema.

## Funcionamento do Sistema

### Principais Componentes
- **Número de robôs:** 3 (R1, R2, R3 - substitui R1 ou R2 em caso de falha).
- **Número de máquinas:** 4 (M1, M2, M3, M4).
- **Buffer de Entrada (BE):** local onde os robôs retiram insumos.

### Regras Operacionais

#### Rotas dos Robôs
- **R1:** Transporta caixas do **BE** para **M1** e **M2**.
- **R2:** Transporta caixas do **BE** para **M3** e **M4**.
- **R3:** Substitui **R1** ou **R2** em caso de falha.

## Modelagem no Supremica

O sistema é modelado usando **autômatos finitos**, representando os robôs, suas restrições e o supervisor. Os eventos são divididos em **controláveis** e **não controláveis**:

### Eventos Controláveis
- `move(Ri, BE, Mx)`: **Ri** transporta uma caixa do **BE** para a máquina **Mx**.
- `unload(Ri, Mx)`: **Ri** entrega a caixa na máquina **Mx**.

### Eventos Não Controláveis
- `request(BE, Mx)`: Nova solicitação de transporte surge.
- `fault(Ri)`: O robô **Ri** apresenta falha.
- `reset(Ri)`: O robô **Ri** volta a funcionar.

## Demonstração

Link de acesso ao vídeo no YouTube: 

## Desenvolvedores

    Mateus Figueiredo (mateus.figueiredo@ee.ufcg.edu.br)
    Matheus Lucas     (matheuslucas.farias@ee.ufcg.edu.br)
    Tâmara Ruth       (tamara.santos@ee.ufcg.edu.br)
