# Click2Mail: Get Cost Estimate

Retrieves a mailing cost estimate from Click2Mail.

```
GET https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-cost-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Click2Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-cost-estimate?connectionId=$CONNECTION_ID&documentClass=string&layout=string&productionTime=string&envelope=string&color=string&paperType=string&printOption=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentClass": "string",
  "layout": "string",
  "productionTime": "string",
  "envelope": "string",
  "color": "string",
  "paperType": "string",
  "printOption": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/click2Mail/latest/actions/get-cost-estimate?${params}`, {
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
| `documentClass` | string | yes | The general type of the product |
| `layout` | string | yes | The specific type of the product |
| `productionTime` | string | yes | The desired production time |
| `envelope` | string | yes | If this is an enveloped product this determines the envelope in which the product is to be mailed; otherwise provide no description |
| `color` | string | yes | Print in color or black and white |
| `paperType` | string | yes | Sets the paper the mailing is to be printed on |
| `printOption` | string | yes | Sets simplex or duplex printing |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mailClass` | string | no | If the product is mailed how do you want it mailed |
| `quantity` | number | no | How many do you want printed Default: `1`. |
| `nonStandardQuantity` | number | no | How may non-standard addresses Default: `1`. |
| `internationalQuantity` | number | no | How many international addresses Default: `1`. |
| `numberOfPages` | number | no | How many pages in your document Default: `1`. |
| `paymentType` | string | no | Default is Credit Card |
| `couponCode` | string | no | Coupon Code |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Click2Mail API, this operation is `GET /molpro/costEstimate` (base URL `https://stage-rest.click2mail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cost-estimate.md) for the provider-specific parameters and requirements.

