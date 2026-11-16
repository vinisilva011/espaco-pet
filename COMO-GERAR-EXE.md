# Espaço Pet — aplicativo para Windows

O projeto foi preparado para virar um aplicativo desktop com Electron. A logo enviada foi usada como ícone do aplicativo e do instalador.

## Gerar o instalador pelo GitHub (recomendado, usando seu Mac)

1. Crie um repositório no GitHub e envie **todo o conteúdo desta pasta** para ele.
2. No GitHub, abra a aba **Actions**.
3. Se aparecer a mensagem para permitir workflows, clique em **I understand my workflows, go ahead and enable them**.
4. Selecione **Gerar instalador Windows**.
5. Clique em **Run workflow** e confirme em **Run workflow**.
6. Aguarde o processo terminar com um visto verde.
7. Abra a execução concluída e baixe o artefato **Espaco-Pet-Windows-Installer**.
8. Dentro do ZIP baixado estará o instalador `Espaço Pet Setup 1.0.0.exe` (o nome pode variar ligeiramente).

## Testar no Mac (opcional)

Com Node.js instalado:
```bash
npm install
npm run app:dev
```

## Observações

- O executável é para Windows 64 bits.
- O aplicativo continua usando o Supabase configurado no projeto; os dados ficam na nuvem.
- A chave `sb_publishable_...` do Supabase é uma chave pública apropriada para uso no frontend. Nunca coloque uma chave `service_role` ou secret no aplicativo.
- O primeiro instalador pode mostrar o aviso do Windows SmartScreen porque não tem assinatura digital. Isso é comum em aplicativos próprios ainda não assinados.
- O instalador não é gerado diretamente pelo Mac: o GitHub Actions compila em um ambiente Windows.
