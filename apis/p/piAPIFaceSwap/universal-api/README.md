# <img src="https://images.mindcloud.co/apps/icons/pi-api_1777066428604.png" alt="PiAPI/FaceSwap logo" width="28" height="28"> PiAPI/FaceSwap: Universal API

Create image, multi-face, and video face-swap tasks on PiAPI and track PiAPI task status through the provider's unified task and account endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piAPIFaceSwap/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piapi.ai
- **Vendor API docs:** https://piapi.ai/docs/doc-678694

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details from PiAPI/FaceSwap. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from PiAPI/FaceSwap by ID. |
| [Image Faceswap](actions/image-faceswap.md) | POST | Creates an image faceswap task in PiAPI/FaceSwap. |
| [List Active Tasks](actions/list-active-tasks.md) | GET | Retrieves active task counts from PiAPI/FaceSwap. |
| [List User Task History](actions/list-user-task-history.md) | GET | Retrieves user task history from PiAPI/FaceSwap. |
| [Multi Faceswap](actions/multi-faceswap.md) | POST | Creates a multi-face faceswap task in PiAPI/FaceSwap. |
| [Video Faceswap](actions/video-faceswap.md) | POST | Creates a video faceswap task in PiAPI/FaceSwap. |

