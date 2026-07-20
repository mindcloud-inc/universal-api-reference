# Prembly: PEP and Sanction

Runs PEP and sanction screening in Prembly.

```
POST https://connect.mindcloud.co/v1/universal/prembly/latest/actions/pep-and-sanction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Prembly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/prembly/latest/actions/pep-and-sanction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prembly/latest/actions/pep-and-sanction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "billing_info": {
        "amount_charged": "string",
        "currency": "string",
        "transaction_id": "string",
        "was_charged": true
      },
      "check_type": [
        "string"
      ],
      "data": {
        "custom_pep_count": 1,
        "custom_sanction_count": 1,
        "is_adverse_media": true,
        "is_pep": true,
        "is_sanctioned": true,
        "name": {
          "pep": [
            {
              "data_source": [
                "Ava Chen"
              ],
              "identification_information": {
                "category_tag": "Ava Chen",
                "country_of_citizenship": "Ava Chen",
                "date_of_birth": "2026-05-07T12:00:00.000Z",
                "educated_at": [
                  "Ava Chen"
                ],
                "image": "Ava Chen",
                "name": "Ava Chen",
                "pep_relationship": [
                  {
                    "image": "Ava Chen",
                    "person": "Ava Chen",
                    "position_held": [
                      "Ava Chen"
                    ],
                    "relationship_basis": "Ava Chen",
                    "type": "Ava Chen"
                  }
                ],
                "pep_status": "Ava Chen",
                "percentage_name_match": 1,
                "position_held": [
                  "Ava Chen"
                ]
              },
              "political_partied": [
                "Ava Chen"
              ],
              "position_and_function": [
                "Ava Chen"
              ]
            }
          ]
        },
        "profile_id": "string",
        "report": "string",
        "rule_evaluation": {
          "auto_flagged": true,
          "requires_manual_review": true,
          "risk_level": "string",
          "rules_triggered": 1,
          "total_rules_evaluated": 1,
          "triggered_rules": [
            {
              "auto_flag": true,
              "reason": "string",
              "require_manual_review": true,
              "rule_id": "string",
              "rule_name": "Ava Chen",
              "severity": "string"
            }
          ]
        }
      },
      "processing_time_ms": 1,
      "reference_id": "string",
      "response_code": "string",
      "searched_name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing_info.amount_charged` | string |  |
| `billing_info.currency` | string |  |
| `billing_info.transaction_id` | string |  |
| `billing_info.was_charged` | boolean |  |
| `check_type[]` | string |  |
| `data.custom_pep_count` | number |  |
| `data.custom_sanction_count` | number |  |
| `data.is_adverse_media` | boolean |  |
| `data.is_pep` | boolean |  |
| `data.is_sanctioned` | boolean |  |
| `data.name.pep[].data_source[]` | string |  |
| `data.name.pep[].identification_information.category_tag` | string |  |
| `data.name.pep[].identification_information.country_of_citizenship` | string |  |
| `data.name.pep[].identification_information.date_of_birth` | date |  |
| `data.name.pep[].identification_information.educated_at[]` | string |  |
| `data.name.pep[].identification_information.image` | string |  |
| `data.name.pep[].identification_information.name` | string |  |
| `data.name.pep[].identification_information.pep_relationship[].image` | string |  |
| `data.name.pep[].identification_information.pep_relationship[].person` | string |  |
| `data.name.pep[].identification_information.pep_relationship[].position_held[]` | string |  |
| `data.name.pep[].identification_information.pep_relationship[].relationship_basis` | string |  |
| `data.name.pep[].identification_information.pep_relationship[].type` | string |  |
| `data.name.pep[].identification_information.pep_status` | string |  |
| `data.name.pep[].identification_information.percentage_name_match` | number |  |
| `data.name.pep[].identification_information.position_held[]` | string |  |
| `data.name.pep[].political_partied[]` | string |  |
| `data.name.pep[].position_and_function[]` | string |  |
| `data.profile_id` | string |  |
| `data.report` | string |  |
| `data.rule_evaluation.auto_flagged` | boolean |  |
| `data.rule_evaluation.requires_manual_review` | boolean |  |
| `data.rule_evaluation.risk_level` | string |  |
| `data.rule_evaluation.rules_triggered` | number |  |
| `data.rule_evaluation.total_rules_evaluated` | number |  |
| `data.rule_evaluation.triggered_rules[].auto_flag` | boolean |  |
| `data.rule_evaluation.triggered_rules[].reason` | string |  |
| `data.rule_evaluation.triggered_rules[].require_manual_review` | boolean |  |
| `data.rule_evaluation.triggered_rules[].rule_id` | string |  |
| `data.rule_evaluation.triggered_rules[].rule_name` | string |  |
| `data.rule_evaluation.triggered_rules[].severity` | string |  |
| `processing_time_ms` | number |  |
| `reference_id` | string |  |
| `response_code` | string |  |
| `searched_name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Prembly API, this operation is `POST /api/v1/verification/aml-screening/` (base URL `https://api.prembly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pep-and-sanction.md) for the provider-specific parameters and requirements.

