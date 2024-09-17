# Sistema de Gerenciamento de Câmeras RTSP

O projeto é de uma aplicação fullstack utilizando **Django** e **React**. O desafio é fornecer um sistema simples e eficiente para gerenciar câmeras de segurança ou monitoramento que utilizam o protocolo **RTSP** (Real-Time Streaming Protocol).

## Descrição da Ideia

A aplicação foi projetada para ambientes onde é necessário monitorar diversas câmeras, permitindo a visualização de streams de vídeo em tempo real. O sistema oferece funcionalidades básica de gerenciamento de streams.
### Principais Funcionalidades

1. **Cadastro e edição de streams**: 
   - O usuário pode adicionar câmeras ao sistema informando um nome descritivo e o link RTSP da câmera.
   - O sistema permite editar tanto o nome da câmera quanto o link RTSP. Isso facilita a atualização de câmeras sem a necessidade de removê-las e cadastrá-las novamente.
   - O usuário pode remover câmeras que não são mais necessárias ou que foram substituídas, mantendo o sistema organizado e atualizado. 
2. **Visualização de Múltiplas Câmeras**: 
   - O sistema oferece uma interface onde até quatro câmeras podem ser visualizadas simultaneamente. Cada câmera exibida mostrará seu stream de vídeo em tempo real, proporcionando uma visualização centralizada e eficiente.

## Tecnologias Utilizadas

### Backend (Django)
- **Django**: Framework utilizado para criar a API RESTful que gerencia as câmeras e seus links RTSP.
- **Django REST Framework (DRF)**: Facilita a criação da API e o gerenciamento de dados.
- **SQLite**: Banco de dados padrão do Django utilizado para armazenar as informações das câmeras (nome e link).

### Frontend (React)
- **React**: Framework JavaScript utilizado para construir a interface de usuário, proporcionando uma experiência dinâmica e interativa.
- **Axios**: Biblioteca usada para fazer as requisições HTTP entre o frontend e o backend, permitindo que o React consuma a API Django.
- **React-Player**: Um player de mídia utilizado para reproduzir os vídeos via links RTSP diretamente na interface React.

### Como Funciona

- O **frontend** em React interage com o **backend** em Django através de requisições HTTP, consumindo a API REST fornecida pelo Django REST Framework. 
- A API gerencia os dados das câmeras (nome e link RTSP) e fornece as operações necessárias para **adicionar**, **editar**, **remover** e **listar** câmeras.
- Quando o usuário deseja visualizar as câmeras, o **React-Player** renderiza o stream de vídeo ao vivo usando os links RTSP fornecidos.

### Fluxo Básico de Uso

1. O usuário acessa a interface do sistema, onde pode adicionar novas câmeras informando seu nome e link RTSP.
2. Após o cadastro, as câmeras aparecem listadas na interface, e o usuário pode selecionar até quatro câmeras para visualizar seus streams simultaneamente.
3. O sistema permite que o usuário altere os dados das câmeras ou remova câmeras que não sejam mais necessárias.
4. A interface de visualização suporta até quatro streams de vídeo simultâneos, organizados em um layout grid, facilitando o monitoramento.

## Ideias de Melhorias Futuras

- **Autenticação de Usuários**: Para garantir a segurança do sistema, o ideal seria inserir uma camada de autenticação com diferentes níveis de autoridade, onde apenas usuários autorizados poderão acessar e gerenciar as câmeras.
- **Suporte a WebSocket**: Para otimizar a visualização dos streams, o uso de WebSocket pode ser adicionado, melhorando a performance e reduzindo latência.
