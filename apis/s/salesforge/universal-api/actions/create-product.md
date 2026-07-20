# Salesforge: Create Product

Creates a product in Salesforge.

```
POST https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "wks_lxxtq91neaixc8yaiqp7w"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "wks_lxxtq91neaixc8yaiqp7w"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | Example: `wks_lxxtq91neaixc8yaiqp7w`. |
| `product` | object | no |  |
| `product.name` | string | no | Example: `Stage 3 Product`. |
| `product.internalName` | string | no | Example: `stage3-product`. |
| `product.language` | list | no | One of: `american_english`, `brazilian_portugese`, `british_english`, `czech`, `danish`, `dutch`, `estonian`, `finnish`, `french`, `german`, `hungarian`, `italian`, `japanese`, `latvian`, `lithuanian`, `norwegian`, `polish`, `romanian`, `russian`, `spanish`, `swedish`, `ukrainian`. Example: `american_english`. |
| `product.industry` | string | no | Example: `Software`. |
| `product.idealCustomerProfile` | string | no | Example: `B2B revenue teams at growth-stage SaaS companies`. |
| `product.pain` | string | no | Example: `Low reply rates from manual outbound workflows`. |
| `product.solution` | string | no | Example: `Automated personalization and sequencing for outbound campaigns`. |
| `product.proofPoints` | string | no | Example: `Used by fast-moving RevOps teams to scale pipeline generation`. |
| `product.costOfInaction` | string | no | Example: `Missed pipeline targets and slower sales cycles`. |
| `translation[]` | array<object> | no |  |
| `translation[].name` | string | no | Example: `Produto Etapa 3`. |
| `translation[].internalName` | string | no | Example: `produto-etapa-3`. |
| `translation[].language` | list | no | One of: `american_english`, `brazilian_portugese`, `british_english`, `czech`, `danish`, `dutch`, `estonian`, `finnish`, `french`, `german`, `hungarian`, `italian`, `japanese`, `latvian`, `lithuanian`, `norwegian`, `polish`, `romanian`, `russian`, `spanish`, `swedish`, `ukrainian`. Example: `brazilian_portugese`. |
| `translation[].industry` | string | no | Example: `Tecnologia`. |
| `translation[].idealCustomerProfile` | string | no | Example: `Equipes de receita B2B em empresas SaaS em crescimento`. |
| `translation[].pain` | string | no | Example: `Baixas taxas de resposta em prospecção manual`. |
| `translation[].solution` | string | no | Example: `Automação de personalização e sequências para campanhas outbound`. |
| `translation[].proofPoints` | string | no | Example: `Usado por equipes de RevOps para escalar geração de pipeline`. |
| `translation[].costOfInaction` | string | no | Example: `Metas de pipeline perdidas e ciclos de venda mais lentos`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internalName": "Ava Chen",
      "translations": [
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
| `id` | string |  |
| `internalName` | string |  |
| `translations` | array<object> |  |

## Native endpoint

Through the native Salesforge API, this operation is `POST /public/v2/workspaces/:workspaceID/products` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.

