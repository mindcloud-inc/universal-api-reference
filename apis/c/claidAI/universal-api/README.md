# <img src="https://images.mindcloud.co/apps/icons/claid-ai_1774977013933.png" alt="Claid AI logo" width="28" height="28"> Claid AI: Universal API

Generate, edit, and manage AI product images and videos

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/claidAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://claid.ai
- **Vendor API docs:** https://docs.claid.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Storage Types](actions/list-storage-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/list-storage-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Ai Fashion Model Job

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Fashion Models Generation Result](actions/get-ai-fashion-models-generation-result.md) | GET | Retrieves an AI fashion model result from Claid AI. |
| [Start AI Fashion Models](actions/start-ai-fashion-models.md) | POST | Starts AI fashion model generation in Claid AI. |

### Ai Image Edit Job

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Edit Generation Result](actions/get-ai-edit-generation-result.md) | GET | Retrieves an AI image edit result from Claid AI. |
| [Start AI Image Edit](actions/start-ai-image-edit.md) | POST | Starts an AI image edit in Claid AI. |

### Batch Image Edit Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Image Edit Results](actions/get-batch-image-edit-results.md) | GET | Retrieves batch image edit results from Claid AI. |
| [Process Batch Image Edit](actions/process-batch-image-edit.md) | POST | Starts a batch image edit in Claid AI. |

### Generated Image

| Action | Method | Description |
| --- | --- | --- |
| [Generate Image](actions/generate-image.md) | POST | Creates a generated image in Claid AI. |

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Edit Image](actions/edit-image.md) | POST | Creates an edited image in Claid AI. |
| [Upload Image For Edit](actions/upload-image-for-edit.md) | POST | Creates an edited image in Claid AI from upload. |

### Image Edit Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Image Edit Result](actions/get-async-image-edit-result.md) | GET | Retrieves an asynchronous image edit result from Claid AI. |
| [Start Async Image Edit](actions/start-async-image-edit.md) | POST | Starts an asynchronous image edit in Claid AI. |

### Scene

| Action | Method | Description |
| --- | --- | --- |
| [Create Scene](actions/create-scene.md) | POST | Creates a scene in Claid AI. |

### Storage

| Action | Method | Description |
| --- | --- | --- |
| [Create Storage](actions/create-storage.md) | POST | Creates a storage connector in Claid AI. |
| [Delete Storage](actions/delete-storage.md) | DELETE | Deletes a storage connector from Claid AI by storage ID. |
| [Get Storage](actions/get-storage.md) | GET | Retrieves a storage connector from Claid AI by storage ID. |
| [List Storages](actions/list-storages.md) | GET | Retrieves connected storages from Claid AI. |
| [Update Storage](actions/update-storage.md) | PUT | Updates a storage connector in Claid AI by storage ID. |

### Storage Type

| Action | Method | Description |
| --- | --- | --- |
| [List Storage Types](actions/list-storage-types.md) | GET | Retrieves supported storage types from Claid AI. |

### Video Generation Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Generation Status](actions/get-video-generation-status.md) | GET | Retrieves a video generation result from Claid AI. |
| [Start Video Generation](actions/start-video-generation.md) | POST | Starts a video generation job in Claid AI. |

