# Rossum: Retrieve Suggested Email Recipients

Retrieves suggested email recipients for an annotation in Rossum.

```
GET https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-suggested-email-recipients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-suggested-email-recipients?connectionId=$CONNECTION_ID&annotations%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "annotations[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rossum/latest/actions/retrieve-suggested-email-recipients?${params}`, {
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
| `annotations[]` | array<string> | yes | Annotation URLs to analyze for suggested recipients. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Suggested email recipients returned by Rossum. |

## Native endpoint

Through the native Rossum API, this operation is `POST /annotations/suggested_recipients` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-suggested-email-recipients.md) for the provider-specific parameters and requirements.

