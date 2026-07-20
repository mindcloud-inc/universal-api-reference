# Voiceflow: Get Transcript Property

Retrieves a transcript property from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-property?connectionId=$CONNECTION_ID&propertyId=trprop_123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "trprop_123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-transcript-property?${params}`, {
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
| `propertyId` | string | yes | ID of the property to target. Example: `trprop_123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "property": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "default": true,
        "id": "string",
        "name": "Ava Chen",
        "projectID": "string",
        "type": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `property.createdAt` | date | When the property was created. |
| `property.default` | boolean | Whether this is a default transcript property. |
| `property.id` | string | Transcript property ID. |
| `property.name` | string | Transcript property name. |
| `property.projectID` | string | Voiceflow project ID that owns the property. |
| `property.type` | string | Transcript property value type. |
| `property.updatedAt` | date | When the property was last updated. |

## Native endpoint

Through the native Voiceflow API, this operation is `GET https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transcript-property.md) for the provider-specific parameters and requirements.

