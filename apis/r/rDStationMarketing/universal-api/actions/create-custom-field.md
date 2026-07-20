# RD Station Marketing: Create Custom Field



```
POST https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/create-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/create-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "api_identifier": "string",
  "data_type": "BOOLEAN",
  "label": {},
  "label.pt-BR": "string",
  "name": {},
  "name.pt-BR": "Ava Chen",
  "presentation_type": "CHECK_BOX"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/create-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "api_identifier": "string",
    "data_type": "BOOLEAN",
    "label": {},
    "label.pt-BR": "string",
    "name": {},
    "name.pt-BR": "Ava Chen",
    "presentation_type": "CHECK_BOX"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `api_identifier` | string | yes | Identificador do campo personalizado. |
| `data_type` | list<string> | yes | Tipo de dado do campo. One of: `BOOLEAN`, `INTEGER`, `STRING`, `STRING[]`. |
| `label` | object | yes | Rótulo exibido do campo. |
| `label.pt-BR` | string | yes | Rótulo do campo em formulários no idioma pt-BR. |
| `name` | object | yes | Nome interno do campo. |
| `name.pt-BR` | string | yes | Nome interno do campo no idioma pt-BR. |
| `presentation_type` | list<string> | yes | Tipo de apresentação do campo. One of: `CHECK_BOX`, `COMBO_BOX`, `EMAIL_INPUT`, `MULTIPLE_CHOICE`, `NUMBER_INPUT`, `PHONE_INPUT`, `RADIO_BUTTON`, `TEXT_AREA`, `TEXT_INPUT`, `URL_INPUT`. |
| `validation_rules` | object | no | Regras de validação do campo. |
| `validation_rules.valid_options[]` | array<object> | no | Lista de opções válidas para campos com seleção. |
| `validation_rules.valid_options[].label.pt-BR` | string | no | Rótulo da opção válida em pt-BR. |
| `validation_rules.valid_options[].value` | string | no | Valor interno da opção válida. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiIdentifier": "string",
      "customField": true,
      "dataType": "string",
      "label": {
        "default": "string"
      },
      "name": {
        "default": "Ava Chen"
      },
      "presentationType": "string",
      "uuid": "string",
      "validationRules": {
        "validOptions": [
          {
            "value": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiIdentifier` | string |  |
| `customField` | boolean |  |
| `dataType` | string |  |
| `label.default` | string |  |
| `name.default` | string |  |
| `presentationType` | string |  |
| `uuid` | string |  |
| `validationRules.validOptions[].value` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `POST /platform/contacts/fields` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-field.md) for the provider-specific parameters and requirements.

