# GAN.AI: List Avatars

Retrieves avatars from your GAN.AI account.

```
GET https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GAN.AI `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatars?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gANAI/latest/actions/list-avatars?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDatetime` | string | no |  |
| `startDatetime` | string | no |  |
| `status` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarsList": [
        {
          "avatarId": "string",
          "avatarType": "string",
          "baseVideo": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "estimatedCompletionTime": "string",
          "status": "string",
          "thumbnail": "string",
          "thumbnails": {
            "defaultAlphaMask": "string",
            "defaultBasic": "string",
            "defaultNoBg": "string",
            "landscapeAlphaMask": "string",
            "landscapeBasic": "string",
            "landscapeNoBg": "string",
            "portraitAlphaMask": "string",
            "portraitBasic": "string",
            "portraitNoBg": "string"
          },
          "title": "string"
        }
      ],
      "totalAvatars": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarsList[].avatarId` | string |  |
| `avatarsList[].avatarType` | string |  |
| `avatarsList[].baseVideo` | string |  |
| `avatarsList[].createdAt` | date |  |
| `avatarsList[].estimatedCompletionTime` | string |  |
| `avatarsList[].status` | string |  |
| `avatarsList[].thumbnail` | string |  |
| `avatarsList[].thumbnails.defaultAlphaMask` | string |  |
| `avatarsList[].thumbnails.defaultBasic` | string |  |
| `avatarsList[].thumbnails.defaultNoBg` | string |  |
| `avatarsList[].thumbnails.landscapeAlphaMask` | string |  |
| `avatarsList[].thumbnails.landscapeBasic` | string |  |
| `avatarsList[].thumbnails.landscapeNoBg` | string |  |
| `avatarsList[].thumbnails.portraitAlphaMask` | string |  |
| `avatarsList[].thumbnails.portraitBasic` | string |  |
| `avatarsList[].thumbnails.portraitNoBg` | string |  |
| `avatarsList[].title` | string |  |
| `totalAvatars` | number |  |

## Native endpoint

Through the native GAN.AI API, this operation is `GET /v1/avatars/list` (base URL `https://os.gan.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-avatars.md) for the provider-specific parameters and requirements.

