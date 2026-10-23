# BR Studio VPN

Aplicativo Android nativo em Kotlin para conexão VPN com o protocolo WireGuard.

## Visão geral

Este repositório contém a base estrutural de um aplicativo Android para VPN, com interface moderna em azul e branco, botão de conectar/desconectar, tempo decorrido, status da conexão e seleção de país.

Importante: a VPN só será funcional quando um servidor WireGuard real e validado for configurado e testado em um aparelho Android físico. Nenhuma conexão real deve ser declarada como ativa sem verificação em ambiente real.

## Estrutura do projeto

- `app/src/main/java/com/brstudiovpn/` — código Kotlin do app.
- `app/src/main/res/` — layouts, strings e recursos visuais.
- `app/src/test/java/` — testes unitários.
- `.github/workflows/` — build automatizado para APK de debug.

## Requisitos

- Android Studio Iguana ou superior
- JDK 17
- Android SDK 35
- Emulador ou aparelho Android real com suporte a VPN

## Compilação local

```bash
./gradlew assembleDebug
```

APK gerado em:

```text
app/build/outputs/apk/debug/app-debug.apk
```

## Dependência oficial do WireGuard

```gradle
implementation("com.wireguard.android:tunnel:1.0.20260102")
```

## Segurança

- Não colocar chaves privadas, tokens, senhas ou perfis WireGuard no repositório.
- Não inventar servidores, IPs ou credenciais.
- Não afirmar que a VPN está funcionando sem testes reais em dispositivo físico.
- Não enviar tráfego para servidores que ainda não foram configurados e testados.

## Próximo passo real

Para conectar a um servidor WireGuard real será necessário:

- endereço do servidor;
- porta UDP;
- chave pública do servidor;
- chave privada do cliente;
- DNS do túnel;
- rota de rede e configuração do túnel.

Essas informações ficam fora do código e fora do repositório.
