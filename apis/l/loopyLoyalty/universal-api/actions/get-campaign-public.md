# Loopy Loyalty: Get Campaign Public



```
GET https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-campaign-public
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-campaign-public?connectionId=$CONNECTION_ID&id=5fcDywPejwj9QszwngBTKg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "5fcDywPejwj9QszwngBTKg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/get-campaign-public?${params}`, {
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
| `id` | string | yes | Published campaign ID. Example: `5fcDywPejwj9QszwngBTKg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "business": {
        "name": "Ava Chen",
        "website": "string"
      },
      "consentCheckboxEnabled": true,
      "consentEnabled": true,
      "description": "string",
      "design": {
        "backgroundColor": "string",
        "textColor": "string"
      },
      "disableTerms": true,
      "id": "string",
      "rewards[0]": {
        "rewardName": "Ava Chen",
        "stampsRequired": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `business.name` | string | Business name. |
| `business.website` | string | Business website. |
| `consentCheckboxEnabled` | boolean | Whether the enrolment checkbox is enabled. |
| `consentEnabled` | boolean | Whether campaign-level consent is enabled. |
| `description` | string | Public campaign description. |
| `design.backgroundColor` | string | Campaign background color. |
| `design.textColor` | string | Campaign text color. |
| `disableTerms` | boolean | Whether terms are hidden from the public card page. |
| `id` | string | Public campaign ID. |
| `rewards[0].rewardName` | string | Primary reward name. |
| `rewards[0].stampsRequired` | number | Primary reward threshold. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `GET /campaign/public/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-public.md) for the provider-specific parameters and requirements.

