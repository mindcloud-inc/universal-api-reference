# Agent.ai: Get Company Earnings Info

Retrieves company earnings information from Agent.ai by stock symbol.

```
GET https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-company-earnings-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agent.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-company-earnings-info?connectionId=$CONNECTION_ID&company=string&quarter=1&year=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string",
  "quarter": "1",
  "year": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/agentai/latest/actions/get-company-earnings-info?${params}`, {
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
| `company` | string | yes | Stock symbol of the company. |
| `quarter` | number | yes | Quarter of the year to retrieve earnings info. |
| `year` | number | yes | Year of the earnings info to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Company earnings transcript or summary text returned by the action. |
| `status` | number | HTTP status code of the action response. |

## Native endpoint

Through the native Agent.ai API, this operation is `POST /action/company_financial_info` (base URL `https://api-lr.agent.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-earnings-info.md) for the provider-specific parameters and requirements.

