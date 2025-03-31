# Video

Aplicativo React Native com funcionalidade de câmera.

## Descrição

Este aplicativo utiliza a câmera do dispositivo para capturar fotos. Ele permite alternar entre as câmeras frontal e traseira, tirar fotos e exibi-las em um modal. O aplicativo também solicita permissões de câmera ao usuário.

---

## Funcionalidades

- **Captura de Fotos**: Permite tirar fotos usando a câmera do dispositivo.
- **Alternar Câmera**: Alterna entre a câmera frontal e traseira.
- **Exibição de Foto**: Exibe a foto capturada em um modal.
- **Solicitação de Permissões**: Solicita permissões de câmera ao usuário.

---

## Estrutura do Código

### Importações

- **React e Hooks**: `useState`, `useEffect`, `useRef` para gerenciar estado e efeitos.
- **Componentes do React Native**: `View`, `SafeAreaView`, `TouchableOpacity`, `Modal`, `Image`, `Button`.
- **Expo Camera**: `CameraView`, `useCameraPermissions` para acessar a câmera.
- **Ícones**: `FontAwesome` para ícones visuais.

### Hooks e Estados

- `camRef`: Referência para a câmera.
- `facing`: Estado para alternar entre câmera frontal e traseira.
- `permission`: Estado para verificar se as permissões foram concedidas.
- `capturedPhoto`: Armazena o URI da foto capturada.
- `open`: Controla a visibilidade do modal.

---

## Fluxo do Aplicativo

1. **Solicitação de Permissões**:
   - O `useEffect` solicita permissões de câmera ao usuário ao montar o componente.
   - Caso as permissões não sejam concedidas, exibe uma mensagem e um botão para solicitar novamente.

2. **Alternar Câmera**:
   - O botão de alternância chama a função `toggleCameraFacing`, que alterna entre as câmeras frontal e traseira.

3. **Capturar Foto**:
   - O botão de captura chama a função `takePicture`, que utiliza a referência da câmera para capturar uma foto e armazena o URI no estado `capturedPhoto`.

4. **Exibir Foto**:
   - Se uma foto for capturada, ela é exibida em um modal. O modal pode ser fechado com o botão de fechar.

---

## Componentes

### `App`

O componente principal que gerencia a lógica do aplicativo.

#### Funções

- **`toggleCameraFacing`**: Alterna entre a câmera frontal e traseira.
- **`takePicture`**: Captura uma foto usando a câmera.
- **`requestPermission`**: Solicita permissões de câmera ao usuário.

#### Renderização

- Exibe a câmera com botões para alternar e capturar fotos.
- Exibe um modal com a foto capturada.

---

## Estilos

### `container`

- Centraliza o conteúdo verticalmente.

### `camera`

- Define o tamanho da câmera para ocupar toda a tela.

### `contentButtons`

- Define a área dos botões de alternância e captura.

### `buttonFlip`

- Botão para alternar a câmera, posicionado no canto inferior esquerdo.

### `buttonCamera`

- Botão para capturar fotos, posicionado no canto inferior direito.

### `contentModal`

- Centraliza o conteúdo do modal.

### `closeButton`

- Botão para fechar o modal, posicionado no canto superior esquerdo.

### `imgPhoto`

- Define o tamanho da imagem exibida no modal.

---

## Dependências

### Expo

- **expo-camera**: Para acessar a câmera do dispositivo.
- **expo-fontawesome**: Para ícones visuais.

### React Native

- Componentes básicos como `View`, `TouchableOpacity`, `Modal`, etc.

---

## Como Executar

1. **Instalar Dependências**:

   Execute o comando:

   npm install
