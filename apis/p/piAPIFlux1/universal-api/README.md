# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777067675251.png" alt="PiAPI/Flux.1 logo" width="28" height="28"> PiAPI/Flux.1: Universal API

Generate and edit images with PiAPI Flux models

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIFlux1/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves your account information from PiAPI/Flux.1. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Flux ControlNet LoRA Task](actions/create-flux-control-net-lo-ra-task.md) | POST | Creates a Flux ControlNet LoRA task in PiAPI/Flux.1. |
| [Create Flux Fill Inpaint Task](actions/create-flux-fill-inpaint-task.md) | POST | Creates a Flux fill inpaint task in PiAPI/Flux.1. |
| [Create Flux Fill Outpaint Task](actions/create-flux-fill-outpaint-task.md) | POST | Creates a Flux fill outpaint task in PiAPI/Flux.1. |
| [Create Flux Image to Image LoRA Task](actions/create-flux-image-to-image-lo-ra-task.md) | POST | Creates a Flux image-to-image LoRA task in PiAPI/Flux.1. |
| [Create Flux Image to Image Task](actions/create-flux-image-to-image-task.md) | POST | Creates a Flux image-to-image task in PiAPI/Flux.1. |
| [Create Flux Kontext Task](actions/create-flux-kontext-task.md) | POST | Creates a Flux Kontext task in PiAPI/Flux.1. |
| [Create Flux Redux Variation Task](actions/create-flux-redux-variation-task.md) | POST | Creates a Flux Redux variation task in PiAPI/Flux.1. |
| [Create Flux Text to Image LoRA Task](actions/create-flux-text-to-image-lo-ra-task.md) | POST | Creates a Flux text-to-image LoRA task in PiAPI/Flux.1. |
| [Create Flux Text to Image Task](actions/create-flux-text-to-image-task.md) | POST | Creates a Flux text-to-image task in PiAPI/Flux.1. |
| [Get Task](actions/get-task.md) | GET | Retrieves a Flux task from PiAPI/Flux.1. |
| [List Active Tasks](actions/list-active-tasks.md) | GET | Retrieves active task records from PiAPI/Flux.1. |
| [List User Task History](actions/list-user-task-history.md) | GET | Retrieves user task history from PiAPI/Flux.1. |

