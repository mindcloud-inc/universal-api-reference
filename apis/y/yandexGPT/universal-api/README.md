# <img src="https://images.mindcloud.co/apps/icons/favicon-aistudio-yandex-ru-48x48_1776947206362.png" alt="YandexGPT logo" width="28" height="28"> YandexGPT: Universal API

Use Yandex AI Studio to list available models and call YandexGPT through Yandex Cloud.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yandexGPT/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://aistudio.yandex.ru/en
- **Vendor API docs:** https://aistudio.yandex.ru/docs/en/ai-studio/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yandexGPT/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Get Model](actions/get-model.md) | GET |  |
| [List Models](actions/list-models.md) | GET | Lists available AI Studio models in YandexGPT. |

