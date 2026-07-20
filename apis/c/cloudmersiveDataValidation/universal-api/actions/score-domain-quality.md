# Cloudmersive Data Validation: Score Domain Quality

Scores domain quality with Cloudmersive Data Validation.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/score-domain-quality
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Data Validation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/score-domain-quality?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/score-domain-quality?${params}`, {
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
| `domain` | string | yes | Domain name to score. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "DomainQualityScore": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `DomainQualityScore` | number |  |

## Native endpoint

Through the native Cloudmersive Data Validation API, this operation is `POST /validate/domain/quality-score` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/score-domain-quality.md) for the provider-specific parameters and requirements.

