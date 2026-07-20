# Retell AI: Update Phone Number

Updates a phone number in Retell AI.

```
PUT https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-phone-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retell AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-phone-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phoneNumber": "string",
  "inboundAgents[].agentId": "string",
  "inboundAgents[].weight": 1,
  "outboundAgents[].agentId": "string",
  "outboundAgents[].weight": 1,
  "inboundSmsAgents[].agentId": "string",
  "inboundSmsAgents[].weight": 1,
  "outboundSmsAgents[].agentId": "string",
  "outboundSmsAgents[].weight": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retellAI/latest/actions/update-phone-number', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phoneNumber": "string",
    "inboundAgents[].agentId": "string",
    "inboundAgents[].weight": 1,
    "outboundAgents[].agentId": "string",
    "outboundAgents[].weight": 1,
    "inboundSmsAgents[].agentId": "string",
    "inboundSmsAgents[].weight": 1,
    "outboundSmsAgents[].agentId": "string",
    "outboundSmsAgents[].weight": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedInboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowedOutboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `inboundAgents[]` | array<object> | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inboundSmsAgents[]` | array<object> | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `outboundAgents[]` | array<object> | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outboundSmsAgents[]` | array<object> | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `phoneNumber` | string | yes |  |
| `inboundAgentId` | string | no | Unique id of agent to bind to the number. The number will automatically use the agent when receiving inbound calls. If set to null, this number would not accept inbound call. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outboundAgentId` | string | no | Unique id of agent to bind to the number. The number will automatically use the agent when conducting outbound calls. If set to null, this number would not be able to initiate outbound call without agent id override. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `inboundAgentVersion` | number | no | Version of the inbound agent to bind to the number. If not provided, will default to latest version. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outboundAgentVersion` | number | no | Version of the outbound agent to bind to the number. If not provided, will default to latest version. |
| `inboundAgents[]` | array<object> | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inboundAgents[]` | array<object> | no | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inboundAgents[].agentId` | string | yes |  |
| `inboundAgents[].agentVersion` | number | no |  |
| `inboundAgents[].weight` | number | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `outboundAgents[]` | array<object> | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outboundAgents[]` | array<object> | no | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outboundAgents[].agentId` | string | yes |  |
| `outboundAgents[].agentVersion` | number | no |  |
| `outboundAgents[].weight` | number | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `inboundSmsAgents[]` | array<object> | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `inboundSmsAgents[]` | array<object> | no | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `inboundSmsAgents[].agentId` | string | yes |  |
| `inboundSmsAgents[].agentVersion` | number | no |  |
| `inboundSmsAgents[].weight` | number | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `outboundSmsAgents[]` | array<object> | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `outboundSmsAgents[]` | array<object> | no | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `outboundSmsAgents[].agentId` | string | yes |  |
| `outboundSmsAgents[].agentVersion` | number | no |  |
| `outboundSmsAgents[].weight` | number | yes | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `nickname` | string | no | Nickname of the number. This is for your reference only. |
| `inboundWebhookUrl` | string | no | If set, will send a webhook for inbound calls, where you can to override agent id, set dynamic variables and other fields specific to that call. |
| `inboundSmsWebhookUrl` | string | no | If set, will send a webhook for inbound SMS, where you can override agent id, set dynamic variables and other fields specific to that chat. |
| `allowedInboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowedInboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowedOutboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `allowedOutboundCountryList[]` | array<string> | no | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `terminationUri` | string | no | The termination uri to update for the phone number. This is used for outbound calls. |
| `authUsername` | string | no | The username used for authentication for the SIP trunk to update for the phone number. |
| `authPassword` | string | no | The password used for authentication for the SIP trunk to update for the phone number. |
| `transport` | string | no | Outbound transport protocol to update for the phone number. Valid values are "TLS", "TCP" and "UDP". Default is "TCP". |
| `fallbackNumber` | string | no | Enterprise only. Phone number to transfer inbound calls to when organization is in outage mode. Can be either a Retell phone number or an external number. Set to null to remove. Cannot be the same as this phone number, and cannot be a number that already has its own fallback configured (prevents nested forwarding). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedInboundCountryList": [
        "string"
      ],
      "allowedOutboundCountryList": [
        "string"
      ],
      "areaCode": 1,
      "fallbackNumber": "string",
      "inboundAgentId": "string",
      "inboundAgents": [
        {
          "agentId": "string",
          "agentVersion": 1,
          "weight": 1
        }
      ],
      "inboundAgentVersion": 1,
      "inboundSmsAgents": [
        {
          "agentId": "string",
          "agentVersion": 1,
          "weight": 1
        }
      ],
      "inboundSmsWebhookUrl": "https://example.com",
      "inboundWebhookUrl": "https://example.com",
      "lastModificationTimestamp": 1,
      "nickname": "Ava Chen",
      "outboundAgentId": "string",
      "outboundAgents": [
        {
          "agentId": "string",
          "agentVersion": 1,
          "weight": 1
        }
      ],
      "outboundAgentVersion": 1,
      "outboundSmsAgents": [
        {
          "agentId": "string",
          "agentVersion": 1,
          "weight": 1
        }
      ],
      "phoneNumber": "string",
      "phoneNumberPretty": "string",
      "phoneNumberType": "string",
      "sipOutboundTrunkConfig": {
        "authUsername": "Ava Chen",
        "terminationUri": "string",
        "transport": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedInboundCountryList` | array<string> | List of ISO 3166-1 alpha-2 country codes from which inbound calls are allowed. If not set or empty, calls from all countries are allowed. |
| `allowedOutboundCountryList` | array<string> | List of ISO 3166-1 alpha-2 country codes to which outbound calls are allowed. If not set or empty, calls to all countries are allowed. |
| `areaCode` | number | Area code of the number to obtain. Format is a 3 digit integer. Currently only supports US area code. |
| `fallbackNumber` | string | Enterprise only. Phone number to transfer inbound calls to when organization is in outage mode. Can be either a Retell phone number or an external number. Cannot be the same as this phone number, and cannot be a number that already has its own fallback configured (prevents nested forwarding). |
| `inboundAgentId` | string | Unique id of agent to bind to the number. The number will automatically use the agent when receiving inbound calls. If null, this number would not accept inbound call. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `inboundAgents` | array<object> | Inbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_agent_id. |
| `inboundAgents[].agentId` | string |  |
| `inboundAgents[].agentVersion` | number |  |
| `inboundAgents[].weight` | number | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `inboundAgentVersion` | number | Version of the inbound agent to bind to the number. If not provided, will default to latest version. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `inboundSmsAgents` | array<object> | Inbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each inbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to inbound_sms_agent_id. |
| `inboundSmsAgents[].agentId` | string |  |
| `inboundSmsAgents[].agentVersion` | number |  |
| `inboundSmsAgents[].weight` | number | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `inboundSmsWebhookUrl` | string | If set, will send a webhook for inbound SMS, where you can override agent id, set dynamic variables and other fields specific to that chat. |
| `inboundWebhookUrl` | string | If set, will send a webhook for inbound calls, where you can to override agent id, set dynamic variables and other fields specific to that call. |
| `lastModificationTimestamp` | number | Last modification timestamp (milliseconds since epoch). Either the time of last update or creation if no updates available. |
| `nickname` | string | Nickname of the number. This is for your reference only. |
| `outboundAgentId` | string | Unique id of agent to bind to the number. The number will automatically use the agent when conducting outbound calls. If null, this number would not be able to initiate outbound call without agent id override. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outboundAgents` | array<object> | Outbound agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound call, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_agent_id. |
| `outboundAgents[].agentId` | string |  |
| `outboundAgents[].agentVersion` | number |  |
| `outboundAgents[].weight` | number | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `outboundAgentVersion` | number | Version of the outbound agent to bind to the number. If not provided, will default to latest version. Deprecated. See https://docs.retellai.com/deprecation-notice/2026/03-31_phone_number_agent_fields |
| `outboundSmsAgents` | array<object> | Outbound SMS agents to bind to the number with weights. If set and non-empty, one agent will be picked randomly for each outbound SMS, with probability proportional to the weight. Total weights must add up to 1. If not set or empty, fallback to outbound_sms_agent_id. |
| `outboundSmsAgents[].agentId` | string |  |
| `outboundSmsAgents[].agentVersion` | number |  |
| `outboundSmsAgents[].weight` | number | The weight of the agent. When used in a list of agents, the total weights must add up to 1. |
| `phoneNumber` | string | E.164 format of the number (+country code, then number with no space, no special characters), used as the unique identifier for phone number APIs. |
| `phoneNumberPretty` | string | Pretty printed phone number, provided for your reference. |
| `phoneNumberType` | string | Type of the phone number. Allowed values: retell-twilio, retell-telnyx, custom. |
| `sipOutboundTrunkConfig` | object |  |
| `sipOutboundTrunkConfig.authUsername` | string | The username used for authenticating the SIP trunk for the phone number. |
| `sipOutboundTrunkConfig.terminationUri` | string | The termination URI for the SIP trunk for the phone number. |
| `sipOutboundTrunkConfig.transport` | string | Outbound transport protocol for the SIP trunk for the phone number. Valid values are "TLS", "TCP" and "UDP". Default is "TCP". |

## Native endpoint

Through the native Retell AI API, this operation is `PATCH /update-phone-number/{phone_number}` (base URL `https://api.retellai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-phone-number.md) for the provider-specific parameters and requirements.

