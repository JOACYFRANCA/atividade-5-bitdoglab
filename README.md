# Atividade 5 – Foreground/Background com BitDogLab

Este projeto simula uma fila de atendimento usando uma matriz de LEDs WS2812 (NeoPixel), botões e joystick, empregando os conceitos de execução em Foreground e Background com núcleos múltiplos do RP2040.

---

## 🎯 Objetivo da Atividade

- Implementar uma lógica de controle de fila com prioridade.
- Utilizar dois núcleos do microcontrolador:
  - Núcleo 0 (background): espera por interrupções.
  - Núcleo 1 (foreground): trata eventos e atualiza LEDs.
- Simular uma matriz visual da fila usando LEDs WS2812.
- Utilizar botões físicos da placa para controle da fila.

---

## ⚙️ Componentes Utilizados

- **Placa BitDogLab** com microcontrolador RP2040
- **Botão A (GPIO 5)** – Adiciona à fila
- **Botão B (GPIO 6)** – Remove da fila
- **Joystick (GPIO 22)** – Reseta a fila
- **LED RGB Externo (GPIOs 11, 12, 13)** – Indicação de status
- **Matriz WS2812 (GPIO 7)** – Representação gráfica da fila
- **PIO (State Machine)** – Controle da matriz NeoPixel

---

## 🔧 Como Compilar e Executar (BitDogLab)

1. Clone o repositório:
   ```bash
   git clone https://github.com/JOACYFRANCA/atividade-5-bitdoglab.git
   ```
2. Abra a pasta no VSCode com o ambiente do **Pico SDK** configurado.
3. Compile com:
   ```
   Ctrl+Shift+P → CMake: Build
   ```
4. Conecte a BitDogLab via USB e envie o `.uf2`.
5. Abra o monitor serial (baud: 115200) para visualizar os eventos.

---

## 👨‍💻 Autor

**Joacy Raimundo França**  
📧 joacy.franca@hotmail.com  
🎓 Projeto desenvolvido como parte da disciplina de Sistemas Embarcados.

---

**Licença**: Projeto acadêmico de uso livre com fins educacionais.