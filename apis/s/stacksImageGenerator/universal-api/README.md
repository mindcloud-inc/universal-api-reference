# <img src="https://images.mindcloud.co/apps/icons/eight-stacks-image-generator_1775845213288.png" alt="88stacks Image Generator logo" width="28" height="28"> 88stacks Image Generator: Universal API

Generate images and train image generation models with the 88stacks API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stacksImageGenerator/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://88stacks.com/
- **Vendor API docs:** https://88stacks.com/docs/1.0.en.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Models](actions/list-models.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacksImageGenerator/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Image](actions/create-image.md) | POST | Creates images in 88stacks Image Generator from a prompt. |
| [List Invokes](actions/list-invokes.md) | GET | Retrieves image generation requests for a model in 88stacks Image Generator. |

### Models

| Action | Method | Description |
| --- | --- | --- |
| [Create Model](actions/create-model.md) | POST | Creates a new image generation model in 88stacks Image Generator. |
| [Get Model](actions/get-model.md) | GET | Retrieves an image generation model from 88stacks Image Generator. |
| [List Models](actions/list-models.md) | GET | Retrieves image generation models from 88stacks Image Generator. |
| [Update Model](actions/update-model.md) | PUT | Updates an existing image generation model in 88stacks Image Generator. |

