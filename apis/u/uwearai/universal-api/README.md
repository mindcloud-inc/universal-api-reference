# <img src="https://images.mindcloud.co/apps/icons/unnamed-11_1774874065695.png" alt="Uwear.ai logo" width="28" height="28"> Uwear.ai: Universal API

Generate fashion images, videos, clothing items, and avatars

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/uwearai/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://uwear.ai
- **Vendor API docs:** https://docs.dev.uwear.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Clothing Items](actions/get-all-clothing-items.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uwearai/latest/actions/get-all-clothing-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Avatar

| Action | Method | Description |
| --- | --- | --- |
| [Delete Avatar](actions/delete-avatar.md) | DELETE | Deletes an existing avatar from Uwear.ai. |
| [Get All Avatars](actions/get-all-avatars.md) | GET | Retrieves avatars from Uwear.ai. |
| [Get Avatar Details](actions/get-avatar-details.md) | GET | Retrieves avatar details from Uwear.ai. |
| [Save Avatar](actions/save-avatar.md) | POST | Creates an avatar from a generation result in Uwear.ai. |
| [Update Avatar](actions/update-avatar.md) | PUT | Updates an existing avatar in Uwear.ai. |

### Avatar Generation

| Action | Method | Description |
| --- | --- | --- |
| [Create Avatar](actions/create-avatar.md) | POST | Creates an avatar generation in Uwear.ai. |

### Clothing Item

| Action | Method | Description |
| --- | --- | --- |
| [Create New Clothing Item](actions/create-new-clothing-item.md) | POST | Creates a new clothing item in Uwear.ai. |
| [Delete Clothing Item](actions/delete-clothing-item.md) | DELETE | Deletes an existing clothing item from Uwear.ai. |
| [Get All Clothing Items](actions/get-all-clothing-items.md) | GET | Retrieves clothing items from Uwear.ai. |
| [Get Clothing Item Details](actions/get-clothing-item-details.md) | GET | Retrieves clothing item details from Uwear.ai. |
| [Update Clothing Item](actions/update-clothing-item.md) | PUT | Updates an existing clothing item in Uwear.ai. |

### Edited Generation

| Action | Method | Description |
| --- | --- | --- |
| [Create Edit](actions/create-edit.md) | POST | Creates an edited generation in Uwear.ai. |

### Generated Video

| Action | Method | Description |
| --- | --- | --- |
| [Create Video](actions/create-video.md) | POST | Creates a video generation in Uwear.ai. |

### Generation Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Generation](actions/create-generation.md) | POST | Creates a generation in Uwear.ai. |
| [Get All Generations](actions/get-all-generations.md) | GET | Retrieves generations from Uwear.ai. |
| [Get Generation Details](actions/get-generation-details.md) | GET | Retrieves generation details from Uwear.ai. |

### Generation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get All Generation Results](actions/get-all-generation-results.md) | GET | Retrieves generation results from Uwear.ai. |
| [Get Generation Result Details](actions/get-generation-result-details.md) | GET | Retrieves generation result details from Uwear.ai. |

### Upscaled Media

| Action | Method | Description |
| --- | --- | --- |
| [Create Upscale](actions/create-upscale.md) | POST | Creates an upscale generation in Uwear.ai. |

