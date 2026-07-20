# QuestionPro Surveys: Get Image



```
GET https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuestionPro Surveys `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-image?connectionId=$CONNECTION_ID&imageId=4161542" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "4161542"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/questionProSurveys/latest/actions/get-image?${params}`, {
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
| `imageId` | number | yes | The QuestionPro image ID. Example: `4161542`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageID": 1,
      "imageURL": "https://example.com",
      "size": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageID` | number |  |
| `imageURL` | string |  |
| `size` | string |  |

## Native endpoint

Through the native QuestionPro Surveys API, this operation is `GET images/:imageId` (base URL `https://api.questionpro.com/a/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.

