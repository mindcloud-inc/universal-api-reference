# Fairing: List Responses

Retrieves responses from Fairing.

```
GET https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-responses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fairing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-responses?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fairing/latest/actions/list-responses?${params}`, {
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
| `questionId` | number | no | Only return responses for the specified Fairing question ID. |
| `since` | date | no | ISO8601 timestamp used to fetch responses newer than this value. |
| `until` | date | no | ISO8601 timestamp used to fetch responses older than this value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | string | no | Response ID cursor used to fetch the page before the referenced response. |
| `after` | string | no | Response ID cursor used to fetch the page after the referenced response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "couponAmount": "string",
      "couponCode": "string",
      "couponType": "string",
      "customerId": "string",
      "customerOrderCount": 1,
      "email": "ava@example.com",
      "id": "string",
      "insertedAt": "2026-05-07T12:00:00.000Z",
      "landingPagePath": "string",
      "orderCurrencyCode": "string",
      "orderId": "string",
      "orderNumber": "string",
      "orderPlatform": "string",
      "orderSource": "string",
      "orderTotal": "string",
      "orderTotalUsd": "string",
      "other": true,
      "otherResponse": "string",
      "question": "string",
      "questionId": 1,
      "questionType": "string",
      "referringQuestion": "string",
      "referringQuestionId": 1,
      "referringQuestionResponse": "string",
      "referringQuestionResponseId": "string",
      "referringSite": "string",
      "response": "string",
      "responseId": "string",
      "responsePosition": 1,
      "responseProvidedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "utmCampaign": "string",
      "utmContent": "string",
      "utmMedium": "string",
      "utmSource": "string",
      "utmTerm": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `couponAmount` | string | Coupon amount associated with the response. |
| `couponCode` | string | Coupon code associated with the response. |
| `couponType` | string | Coupon type associated with the response. |
| `customerId` | string | Customer identifier associated with the response. |
| `customerOrderCount` | number | Order count for the responding customer. |
| `email` | string | Customer email associated with the response. |
| `id` | string | Fairing response ID. |
| `insertedAt` | date | When the response record was created. |
| `landingPagePath` | string | Landing page path for the response session. |
| `orderCurrencyCode` | string | Currency code for the order total. |
| `orderId` | string | Order ID associated with the response. |
| `orderNumber` | string | Order number associated with the response. |
| `orderPlatform` | string | Commerce platform associated with the order. |
| `orderSource` | string | Order source associated with the response. |
| `orderTotal` | string | Order total associated with the response. |
| `orderTotalUsd` | string | Order total converted to USD. |
| `other` | boolean | Whether the response was submitted as free-form text. |
| `otherResponse` | string | Free-form response text when Other was used. |
| `question` | string | Question text associated with the response. |
| `questionId` | number | ID of the associated Fairing question. |
| `questionType` | string | Question type associated with the response. |
| `referringQuestion` | string | Parent question text for clarification responses. |
| `referringQuestionId` | number | Parent question ID for clarification responses. |
| `referringQuestionResponse` | string | Parent response value for clarification responses. |
| `referringQuestionResponseId` | string | Parent response ID for clarification responses. |
| `referringSite` | string | Referring site for the response session. |
| `response` | string | Selected response value. |
| `responseId` | string | ID of the selected predefined response. |
| `responsePosition` | number | Position of the selected response option. |
| `responseProvidedAt` | date | When the response was provided by the customer. |
| `updatedAt` | date | When the response record was last updated. |
| `utmCampaign` | string | UTM campaign associated with the response. |
| `utmContent` | string | UTM content associated with the response. |
| `utmMedium` | string | UTM medium associated with the response. |
| `utmSource` | string | UTM source associated with the response. |
| `utmTerm` | string | UTM term associated with the response. |

## Native endpoint

Through the native Fairing API, this operation is `GET /responses` (base URL `https://app.fairing.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-responses.md) for the provider-specific parameters and requirements.

