# ads

Repositório de anúncios house para o app **PalmFit**.  
Edite os arquivos aqui e o app buscará automaticamente as mudanças sem novo release.

## Estrutura

```
ads/
├── house_ads.json       ← lista de anúncios consumida pelo app
└── ads/
    └── lista_certa_icon.png   ← ícones dos apps anunciados
```

## Como adicionar um novo anúncio

1. Coloque o ícone do app em `ads/nome_do_app_icon.png`
2. Adicione um objeto no array `ads` do `house_ads.json`:

```json
{
  "id": "nome_unico",
  "name": "Nome Exibido",
  "iconAsset": "https://raw.githubusercontent.com/SEU_USUARIO/ads/main/ads/nome_do_app_icon.png",
  "playStoreUrl": "https://play.google.com/store/apps/details?id=com.pacote.do.app"
}
```

3. Faça commit e push na branch `main`.  
   O app buscará a nova versão no próximo ciclo de 30 segundos.

## Como remover um anúncio

Basta remover o objeto do array e fazer push.  
Não é necessário atualizar o app na Play Store.
