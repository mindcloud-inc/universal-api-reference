# <img src="https://images.mindcloud.co/apps/icons/pi-apiwanx_1776108623390.png" alt="PiAPI/Wanx logo" width="28" height="28"> PiAPI/Wanx: Universal API

Generate WanX videos and retrieve task results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIWanx/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/wanx-api/create-task

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account info from PiAPI/Wanx. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Image to Video with Camera Control](actions/create-image-to-video-control-camera.md) | POST | Creates a camera-controlled video task in PiAPI/Wanx. |
| [Create Image to Video with Keyframes](actions/create-image-to-video-keyframe.md) | POST | Creates a keyframed image-to-video task in PiAPI/Wanx. |
| [Create Image to Video (Wan 2.2)](actions/create-image-to-video-wan22.md) | POST | Creates an image-to-video task in PiAPI/Wanx. |
| [Create Image to Video (14B)](actions/create-image-to-video14b.md) | POST | Creates an image-to-video task in PiAPI/Wanx. |
| [Create Image to Video with LoRA](actions/create-image-to-video14b-lora.md) | POST | Creates a LoRA image-to-video task in PiAPI/Wanx. |
| [Create Text to Video (Wan 2.2)](actions/create-text-to-video-wan22.md) | POST | Creates a text-to-video task in PiAPI/Wanx. |
| [Create Text to Video (1.3B)](actions/create-text-to-video13b.md) | POST | Creates a text-to-video task in PiAPI/Wanx. |
| [Create Text to Video (14B)](actions/create-text-to-video14b.md) | POST | Creates a text-to-video task in PiAPI/Wanx. |
| [Create Text to Video with LoRA](actions/create-text-to-video14b-lora.md) | POST | Creates a LoRA text-to-video task in PiAPI/Wanx. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from PiAPI/Wanx by ID. |

