# Datarobot: List Custom Models

Retrieves a list of custom models from Datarobot.

```
GET https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datarobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datarobot/latest/actions/list-custom-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "deploymentsCount": 1,
      "description": "string",
      "id": "string",
      "language": "string",
      "latestVersion": {},
      "name": "Ava Chen",
      "supportsBinaryClassification": true,
      "supportsRegression": true,
      "targetType": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "userProvidedId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | ISO-8601 timestamp of when the custom model was created. |
| `createdBy` | string | The username of the custom model creator. |
| `deploymentsCount` | number | The number of deployments for the custom model. |
| `description` | string | The description of the custom model. |
| `id` | string | The ID of the custom model. |
| `language` | string | The programming language used to write the model. |
| `latestVersion` | object | The latest version of the custom model. |
| `name` | string | The name of the custom model. |
| `supportsBinaryClassification` | boolean | Whether the model supports binary classification. |
| `supportsRegression` | boolean | Whether the model supports regression. |
| `targetType` | string | The target type of the custom model. |
| `updated` | date | ISO-8601 timestamp of when the custom model was last updated. |
| `userProvidedId` | string | A user-provided unique ID associated with the custom model. |

## Native endpoint

Through the native Datarobot API, this operation is `GET /customModels/` (base URL `https://app.datarobot.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-models.md) for the provider-specific parameters and requirements.

