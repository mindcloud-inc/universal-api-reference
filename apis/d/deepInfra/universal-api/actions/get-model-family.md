# Deep Infra: Get Model Family



```
GET https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-family
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deep Infra `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-family?connectionId=$CONNECTION_ID&familyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "familyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepInfra/latest/actions/get-model-family?${params}`, {
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
| `familyName` | string | yes | Model family name from the model family URL path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "models": {
        "model_name": "Ava Chen"
      },
      "name": "Ava Chen",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Model family description. |
| `models` | array<object> | Models in this family when returned. |
| `models.model_name` | string | Model identifier in the family. |
| `name` | string | Model family slug. |
| `title` | string | Model family display title. |

## Native endpoint

Through the native Deep Infra API, this operation is `GET /model-families/:family_name` (base URL `https://api.deepinfra.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-model-family.md) for the provider-specific parameters and requirements.

