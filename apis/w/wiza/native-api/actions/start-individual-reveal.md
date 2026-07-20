# Start Individual Reveal with Wiza

Starts an individual reveal in Wiza.

## Endpoint

- **Method:** `POST`
- **Path:** `/individual_reveals`
- **Base URL:** `https://wiza.co/api`
- **Official documentation:** [Start Individual Reveal](https://docs.wiza.co/api-reference/individual-reveals/start-individual-reveal)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `individual_reveal` | body | `object` | yes | Object payload describing the person to enrich. |
| `callback_url` | body | `string` | no | Webhook URL to receive async reveal updates. |
| `enrichment_level` | body | `string` | no | Optional reveal enrichment level: none, partial, phone, or full. |
