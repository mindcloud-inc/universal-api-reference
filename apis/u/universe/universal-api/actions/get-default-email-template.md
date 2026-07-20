# Universe: Get Default Email Template

Retrieves the default email template from Universe.

```
GET https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-default-email-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-default-email-template?connectionId=$CONNECTION_ID&query=query%20GetDefaultEmailTemplate(%24eventId%3A%20ID!)%20%7B%0A%20%20defaultEmailTemplate(listingId%3A%20%24eventId)%20%7B%0A%20%20%20%20id%0A%20%20%20%20name%0A%20%20%20%20subject%0A%20%20%20%20isDefault%0A%20%20%20%20updatedAt%0A%20%20%20%20title%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20text%0A%20%20%20%20%20%20color%0A%20%20%20%20%20%20backgroundColor%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "query GetDefaultEmailTemplate($eventId: ID!) {\n  defaultEmailTemplate(listingId: $eventId) {\n    id\n    name\n    subject\n    isDefault\n    updatedAt\n    title {\n      id\n      text\n      color\n      backgroundColor\n    }\n  }\n}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universe/latest/actions/get-default-email-template?${params}`, {
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
| `query` | string | yes | Universe GraphQL query document to execute for this action. Default: `query GetDefaultEmailTemplate($eventId: ID!) {\n  defaultEmailTemplate(listingId: $eventId) {\n    id\n    name\n    subject\n    isDefault\n    updatedAt\n    title {\n      id\n      text\n      color\n      backgroundColor\n    }\n  }\n}`. |
| `variables` | object | no | Optional GraphQL variables object for the default email template query. Default: `{"eventId":"69bc5bb99abe4b003ceea74f"}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Universe API returns.

## Native endpoint

Through the native Universe API, this operation is `POST /graphql` (base URL `https://www.universe.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-default-email-template.md) for the provider-specific parameters and requirements.

