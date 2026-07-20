# SignalWire: Native API Reference

A consolidated summary of SignalWire's API configuration and 120 documented operations, with links to official documentation.

- **Official docs:** https://signalwire.com/docs/apis
- **API base URL:** `https://mindcloud.signalwire.com/api`

## Authentication

### Basic Auth

Connect using SignalWire Basic auth. Enter your Project ID as Username and your API Token as Password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.signalwire.com/rest/overview/authorization/)

## Endpoints (120 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign a resource as a call handler for a Domain Application.](actions/assign-a-resource-as-a-call-handler-for-a-domain-application.md) | `POST /fabric/resources/{id}/domain_applications` | [docs](https://signalwire.com/docs/apis/rest/domain-applications/assign-resource-domain-application) |
| [Assign a Resource to a Phone Route](actions/assign-a-resource-to-a-phone-route.md) | `POST /fabric/resources/{id}/phone_routes` | [docs](https://signalwire.com/docs/apis/rest/phone-numbers/assign-resource-phone-route) |
| [Assign a Resource to a SIP endpoint](actions/assign-a-resource-to-a-sip-endpoint.md) | `POST /fabric/resources/sip_endpoints/resources/{id}/sip_endpoints` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/assign-resource-to-sip-credential) |
| [Create a Document](actions/create-a-document.md) | `POST /datasphere/documents` | [docs](https://signalwire.com/docs/apis/rest/documents/create-document) |
| [Create AI Agent](actions/create-ai-agent.md) | `POST /fabric/resources/ai_agents` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/create-ai-agent) |
| [Create Call Flow](actions/create-call-flow.md) | `POST /fabric/resources/call_flows` | [docs](https://signalwire.com/docs/apis/rest/call-flows/create-call-flow) |
| [Create Chat Token](actions/create-chat-token.md) | `POST /chat/tokens` | [docs](https://signalwire.com/docs/apis/rest/chat-tokens/create-chat-token) |
| [Create Conference Room](actions/create-conference-room.md) | `POST /fabric/resources/conference_rooms` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/create-conference-room) |
| [Create cXML Script](actions/create-cxml-script.md) | `POST /fabric/resources/cxml_scripts` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/create-cxml-script) |
| [Create cXML Webhook](actions/create-cxml-webhook.md) | `POST /fabric/resources/cxml_webhooks` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/create-cxml-webhook) |
| [Create FreeSWITCH Connector](actions/create-freeswitch-connector.md) | `POST /fabric/resources/freeswitch_connectors` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/create-freeswitch-connector) |
| [Create Guest Embed Token](actions/create-guest-embed-token.md) | `POST /fabric/embeds/tokens` | [docs](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-guest-embed-token) |
| [Create PubSub Token](actions/create-pubsub-token.md) | `POST /pubsub/tokens` | [docs](https://signalwire.com/docs/apis/rest/pubsub/create-token) |
| [Create Relay Application](actions/create-relay-application.md) | `POST /fabric/resources/relay_applications` | [docs](https://signalwire.com/docs/apis/rest/relay-application/create-relay-application) |
| [Create SIP Endpoint](actions/create-sip-endpoint.md) | `POST /fabric/resources/sip_endpoints` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/create-sip-credential) |
| [Create SIP Gateway](actions/create-sip-gateway.md) | `POST /fabric/resources/sip_gateways` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/create-sip-gateway) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /fabric/resources/subscribers` | [docs](https://signalwire.com/docs/apis/rest/subscribers/create-subscriber) |
| [Create Subscriber Guest Token](actions/create-subscriber-guest-token.md) | `POST /fabric/guests/tokens` | [docs](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-guest-token) |
| [Create Subscriber Invite Token](actions/create-subscriber-invite-token.md) | `POST /fabric/subscriber/invites` | [docs](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-invite-token) |
| [Create Subscriber SIP Endpoint](actions/create-subscriber-sip-endpoint.md) | `POST /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints` | [docs](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/create-subscriber-sip-credential) |
| [Create Subscriber Token](actions/create-subscriber-token.md) | `POST /fabric/subscribers/tokens` | [docs](https://signalwire.com/docs/apis/rest/subscribers/tokens/create-subscriber-token) |
| [Create SWML Script](actions/create-swml-script.md) | `POST /fabric/resources/swml_scripts` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/create-swml-script) |
| [Create SWML Webhook](actions/create-swml-webhook.md) | `POST /fabric/resources/swml_webhooks` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/create-swml-webhook) |
| [Delete a Document](actions/delete-a-document.md) | `DELETE /datasphere/documents/{id}` | [docs](https://signalwire.com/docs/apis/rest/documents/delete-document) |
| [Delete AI Agent](actions/delete-ai-agent.md) | `DELETE /fabric/resources/ai_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/delete-ai-agent) |
| [Delete Call Flow](actions/delete-call-flow.md) | `DELETE /fabric/resources/call_flows/{id}` | [docs](https://signalwire.com/docs/apis/rest/call-flows/delete-call-flow) |
| [Delete Chunk](actions/delete-chunk.md) | `DELETE /datasphere/documents/{documentId}/chunks/{chunkId}` | [docs](https://signalwire.com/docs/apis/rest/chunks/delete-document-chunk) |
| [Delete Conference Room](actions/delete-conference-room.md) | `DELETE /fabric/resources/conference_rooms/{id}` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/delete-conference-room) |
| [Delete cXML Application](actions/delete-cxml-application.md) | `DELETE /fabric/resources/cxml_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-applications/delete-cxml-application) |
| [Delete cXML Script](actions/delete-cxml-script.md) | `DELETE /fabric/resources/cxml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/delete-cxml-script) |
| [Delete cXML Webhook](actions/delete-cxml-webhook.md) | `DELETE /fabric/resources/cxml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/delete-cxml-webhook) |
| [Delete Dialogflow Agent](actions/delete-dialogflow-agent.md) | `DELETE /fabric/resources/dialogflow_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/delete-dialogflow-agent) |
| [Delete FreeSWITCH Connector](actions/delete-freeswitch-connector.md) | `DELETE /fabric/resources/freeswitch_connectors/{id}` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/delete-freeswitch-connector) |
| [Delete Relay Application](actions/delete-relay-application.md) | `DELETE /fabric/resources/relay_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/relay-application/delete-relay-application) |
| [Delete Resource](actions/delete-resource.md) | `DELETE /fabric/resources/{id}` | [docs](https://signalwire.com/docs/apis/rest/resources/delete-resource) |
| [Delete SIP Endpoint](actions/delete-sip-endpoint.md) | `DELETE /fabric/resources/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/delete-sip-credential) |
| [Delete SIP Gateway](actions/delete-sip-gateway.md) | `DELETE /fabric/resources/sip_gateways/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/delete-sip-gateway) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /fabric/resources/subscribers/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/delete-subscriber) |
| [Delete Subscriber SIP Endpoint](actions/delete-subscriber-sip-endpoint.md) | `DELETE /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/delete-subscriber-sip-credential) |
| [Delete SWML Script](actions/delete-swml-script.md) | `DELETE /fabric/resources/swml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/delete-swml-script) |
| [Delete SWML Webhook](actions/delete-swml-webhook.md) | `DELETE /fabric/resources/swml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/delete-swml-webhook) |
| [Deploy Call Flow Version](actions/deploy-call-flow-version.md) | `POST /fabric/resources/call_flow/{id}/versions` | [docs](https://signalwire.com/docs/apis/rest/call-flows/deploy-call-flow-version) |
| [Get AI Agent](actions/get-ai-agent.md) | `GET /fabric/resources/ai_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/get-ai-agent) |
| [Get Call Flow](actions/get-call-flow.md) | `GET /fabric/resources/call_flows/{id}` | [docs](https://signalwire.com/docs/apis/rest/call-flows/get-call-flow) |
| [Get Conference Room](actions/get-conference-room.md) | `GET /fabric/resources/conference_rooms/{id}` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/get-conference-room) |
| [Get cXML Application](actions/get-cxml-application.md) | `GET /fabric/resources/cxml_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-applications/get-cxml-application) |
| [Get cXML Script](actions/get-cxml-script.md) | `GET /fabric/resources/cxml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/get-cxml-script) |
| [Get cXML Webhook](actions/get-cxml-webhook.md) | `GET /fabric/resources/cxml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/get-cxml-webhook) |
| [Get Dialogflow Agent](actions/get-dialogflow-agent.md) | `GET /fabric/resources/dialogflow_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/get-dialogflow-agent) |
| [Get Fax Log](actions/get-fax-log.md) | `GET /fax/logs/{id}` | [docs](https://signalwire.com/docs/apis/rest/fax-logs/get-fax-log) |
| [Get FreeSWITCH Connector](actions/get-freeswitch-connector.md) | `GET /fabric/resources/freeswitch_connectors/{id}` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/get-freeswitch-connector) |
| [Get Message Log](actions/get-message-log.md) | `GET /messaging/logs/{id}` | [docs](https://signalwire.com/docs/apis/rest/message-logs/get-message-log) |
| [Get Relay Application](actions/get-relay-application.md) | `GET /fabric/resources/relay_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/relay-application/get-relay-application) |
| [Get Resource](actions/get-resource.md) | `GET /fabric/resources/{id}` | [docs](https://signalwire.com/docs/apis/rest/resources/get-resource) |
| [Get SIP Endpoint](actions/get-sip-endpoint.md) | `GET /fabric/resources/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/get-sip-credential) |
| [Get SIP Gateway](actions/get-sip-gateway.md) | `GET /fabric/resources/sip_gateways/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/get-sip-gateway) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /fabric/resources/subscribers/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/get-subscriber) |
| [Get Subscriber SIP Endpoint](actions/get-subscriber-sip-endpoint.md) | `GET /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/get-subscriber-sip-credential) |
| [Get SWML Script](actions/get-swml-script.md) | `GET /fabric/resources/swml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/get-swml-script) |
| [Get SWML Webhook](actions/get-swml-webhook.md) | `GET /fabric/resources/swml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/get-swml-webhook) |
| [Get Voice Log](actions/get-voice-log.md) | `GET /voice/logs/{id}` | [docs](https://signalwire.com/docs/apis/rest/voice-logs/get-voice-log) |
| [List AI Agent Addresses](actions/list-ai-agent-addresses.md) | `GET /fabric/resources/ai_agents/{ai_agent_id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/list-ai-agent-addresses) |
| [List AI Agents](actions/list-ai-agents.md) | `GET /fabric/resources/ai_agents` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/list-ai-agents) |
| [List Call Flow Addresses](actions/list-call-flow-addresses.md) | `GET /fabric/resources/call_flow/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/call-flows/list-call-flow-addresses) |
| [List Call Flow Versions](actions/list-call-flow-versions.md) | `GET /fabric/resources/call_flow/{id}/versions` | [docs](https://signalwire.com/docs/apis/rest/call-flows/list-call-flow-versions) |
| [List Call Flows](actions/list-call-flows.md) | `GET /fabric/resources/call_flows` | [docs](https://signalwire.com/docs/apis/rest/call-flows/list-call-flows) |
| [List Chunks](actions/list-chunks.md) | `GET /datasphere/documents/{documentId}/chunks` | [docs](https://signalwire.com/docs/apis/rest/chunks/list-document-chunks) |
| [List Conference Room Addresses](actions/list-conference-room-addresses.md) | `GET /fabric/resources/conference_room/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/list-conference-room-addresses) |
| [List Conference Rooms](actions/list-conference-rooms.md) | `GET /fabric/resources/conference_rooms` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/list-conference-rooms) |
| [List Conferences](actions/list-conferences.md) | `GET /logs/conferences` | [docs](https://signalwire.com/docs/apis/rest/conference-logs/list-conferences) |
| [List cXML Application Addresses](actions/list-cxml-application-addresses.md) | `GET /fabric/resources/cxml_applications/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/cxml-applications/list-cxml-application-addresses) |
| [List cXML Applications](actions/list-cxml-applications.md) | `GET /fabric/resources/cxml_applications` | [docs](https://signalwire.com/docs/apis/rest/cxml-applications/list-cxml-applications) |
| [List cXML Script Addresses](actions/list-cxml-script-addresses.md) | `GET /fabric/resources/cxml_scripts/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/list-cxml-script-addresses) |
| [List cXML Scripts](actions/list-cxml-scripts.md) | `GET /fabric/resources/cxml_scripts` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/list-cxml-scripts) |
| [List cXML Webhook Addresses](actions/list-cxml-webhook-addresses.md) | `GET /fabric/resources/cxml_webhooks/{cxml_webhook_id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/list-cxml-webhook-addresses) |
| [List cXML Webhooks](actions/list-cxml-webhooks.md) | `GET /fabric/resources/cxml_webhooks` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/list-cxml-webhooks) |
| [List Dialogflow Agent Addresses](actions/list-dialogflow-agent-addresses.md) | `GET /fabric/resources/dialogflow_agents/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/list-dialogflow-agent-addresses) |
| [List Dialogflow Agents](actions/list-dialogflow-agents.md) | `GET /fabric/resources/dialogflow_agents` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/list-dialogflow-agents) |
| [List Documents](actions/list-documents.md) | `GET /datasphere/documents` | [docs](https://signalwire.com/docs/apis/rest/documents/list-documents) |
| [List Fabric Addresses assigned to a SIP Gateway](actions/list-fabric-addresses-assigned-to-a-sip-gateway.md) | `GET /fabric/resources/sip_gateways/resources/sip_gateways/{resource_id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/list-sip-gateway-addresses) |
| [List Fabric Resources](actions/list-fabric-resources.md) | `GET /fabric/resources` | [docs](https://signalwire.com/docs/apis/rest/resources/list-resources) |
| [List Fax Logs](actions/list-fax-logs.md) | `GET /fax/logs` | [docs](https://signalwire.com/docs/apis/rest/fax-logs/list-fax-logs) |
| [List FreeSWITCH Connector Addresses](actions/list-freeswitch-connector-addresses.md) | `GET /fabric/resources/freeswitch_connectors/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/list-freeswitch-connector-addresses) |
| [List FreeSWITCH Connectors](actions/list-freeswitch-connectors.md) | `GET /fabric/resources/freeswitch_connectors` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/list-freeswitch-connectors) |
| [List Log Events](actions/list-log-events.md) | `GET /voice/logs/{id}/events` | [docs](https://signalwire.com/docs/apis/rest/voice-logs/list-voice-log-events) |
| [List Message Logs](actions/list-message-logs.md) | `GET /messaging/logs` | [docs](https://signalwire.com/docs/apis/rest/message-logs/list-message-logs) |
| [List Relay Application Addresses](actions/list-relay-application-addresses.md) | `GET /fabric/resources/relay_applications/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/relay-application/list-relay-application-addresses) |
| [List Relay Applications](actions/list-relay-applications.md) | `GET /fabric/resources/relay_applications` | [docs](https://signalwire.com/docs/apis/rest/relay-application/list-relay-applications) |
| [List Resource Addresses](actions/list-resource-addresses.md) | `GET /fabric/resources/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/addresses/list-resource-addresses-client) |
| [List SIP Endpoint Addresses](actions/list-sip-endpoint-addresses.md) | `GET /fabric/resources/sip_endpoints/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/list-sip-credential-addresses) |
| [List SIP Endpoints](actions/list-sip-endpoints.md) | `GET /fabric/resources/sip_endpoints` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/list-sip-credentials) |
| [List SIP Gateways](actions/list-sip-gateways.md) | `GET /fabric/resources/sip_gateways` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/list-sip-gateways) |
| [List Subscriber Addresses](actions/list-subscriber-addresses.md) | `GET /fabric/resources/subscribers/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/subscribers/list-subscriber-addresses) |
| [List Subscriber SIP Endpoints](actions/list-subscriber-sip-endpoints.md) | `GET /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints` | [docs](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/list-subscriber-sip-credentials) |
| [List Subscribers](actions/list-subscribers.md) | `GET /fabric/resources/subscribers` | [docs](https://signalwire.com/docs/apis/rest/subscribers/list-subscribers) |
| [List SWML Script Addresses](actions/list-swml-script-addresses.md) | `GET /fabric/resources/swml_scripts/{id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/list-swml-script-addresses) |
| [List SWML Scripts](actions/list-swml-scripts.md) | `GET /fabric/resources/swml_scripts` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/list-swml-scripts) |
| [List SWML Webhook Addresses](actions/list-swml-webhook-addresses.md) | `GET /fabric/resources/swml_webhooks/{swml_webhook_id}/addresses` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/list-swml-webhook-addresses) |
| [List SWML Webhooks](actions/list-swml-webhooks.md) | `GET /fabric/resources/swml_webhooks` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/list-swml-webhooks) |
| [List Voice Logs](actions/list-voice-logs.md) | `GET /voice/logs` | [docs](https://signalwire.com/docs/apis/rest/voice-logs/list-voice-logs) |
| [Refresh Subscriber Token](actions/refresh-subscriber-token.md) | `POST /fabric/subscribers/tokens/refresh` | [docs](https://signalwire.com/docs/apis/rest/subscribers/tokens/refresh-subscriber-token) |
| [Retrieve Chunk](actions/retrieve-chunk.md) | `GET /datasphere/documents/{documentId}/chunks/{chunkId}` | [docs](https://signalwire.com/docs/apis/rest/chunks/get-document-chunk) |
| [Search Documents](actions/search-documents.md) | `POST /datasphere/documents/search` | [docs](https://signalwire.com/docs/apis/rest/documents/search-documents) |
| [Send Call Commands](actions/send-call-commands.md) | `POST /calling/calls` | [docs](https://signalwire.com/docs/apis/rest/calls/call-commands) |
| [Update a Document](actions/update-a-document.md) | `PATCH /datasphere/documents/{id}` | [docs](https://signalwire.com/docs/apis/rest/documents/update-document) |
| [Update AI Agent](actions/update-ai-agent.md) | `PATCH /fabric/resources/ai_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-custom/update-ai-agent) |
| [Update Call Flow](actions/update-call-flow.md) | `PUT /fabric/resources/call_flows/{id}` | [docs](https://signalwire.com/docs/apis/rest/call-flows/update-call-flow) |
| [Update Conference Room](actions/update-conference-room.md) | `PUT /fabric/resources/conference_rooms/{id}` | [docs](https://signalwire.com/docs/apis/rest/conference-rooms/update-conference-room) |
| [Update cXML Application](actions/update-cxml-application.md) | `PUT /fabric/resources/cxml_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-applications/update-cxml-application) |
| [Update cXML Script](actions/update-cxml-script.md) | `PUT /fabric/resources/cxml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-scripts/update-cxml-script) |
| [Update cXML Webhook](actions/update-cxml-webhook.md) | `PATCH /fabric/resources/cxml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/cxml-webhook/update-cxml-webhook) |
| [Update Dialogflow Agent](actions/update-dialogflow-agent.md) | `PUT /fabric/resources/dialogflow_agents/{id}` | [docs](https://signalwire.com/docs/apis/rest/ai-agents/ai-agents-dialogflow/update-dialogflow-agent) |
| [Update FreeSWITCH Connector](actions/update-freeswitch-connector.md) | `PUT /fabric/resources/freeswitch_connectors/{id}` | [docs](https://signalwire.com/docs/apis/rest/freeswitch-connector/update-freeswitch-connector) |
| [Update Relay Application](actions/update-relay-application.md) | `PUT /fabric/resources/relay_applications/{id}` | [docs](https://signalwire.com/docs/apis/rest/relay-application/update-relay-application) |
| [Update SIP Endpoint](actions/update-sip-endpoint.md) | `PUT /fabric/resources/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-credentials/update-sip-credential) |
| [Update SIP Gateway](actions/update-sip-gateway.md) | `PATCH /fabric/resources/sip_gateways/{id}` | [docs](https://signalwire.com/docs/apis/rest/sip-gateway/update-sip-gateway) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /fabric/resources/subscribers/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/update-subscriber) |
| [Update Subscriber SIP Endpoint](actions/update-subscriber-sip-endpoint.md) | `PATCH /fabric/resources/subscribers/{fabric_subscriber_id}/sip_endpoints/{id}` | [docs](https://signalwire.com/docs/apis/rest/subscribers/sip-credentials/update-subscriber-sip-credential) |
| [Update SWML Script](actions/update-swml-script.md) | `PUT /fabric/resources/swml_scripts/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-scripts/update-swml-script) |
| [Update SWML Webhook](actions/update-swml-webhook.md) | `PATCH /fabric/resources/swml_webhooks/{id}` | [docs](https://signalwire.com/docs/apis/rest/swml-webhook/update-swml-webhook) |
