# Create Dashboard with Reportei

Creates a new dashboard in Reportei.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboards`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Create Dashboard](https://developers.reportei.com#dashboards-endpoint-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Título do dashboard. |
| `subtitle` | body | `string` | yes | Legenda do dashboard. |
| `start` | body | `date` | yes | Data de início da análise. |
| `end` | body | `date` | yes | Data de fim da análise. |
| `template_id` | body | `number` | yes | ID do template. |
| `integration_ids[]` | body | `array<number>` | yes | Array de IDs das integrações selecionadas. |
| `project_id` | body | `number` | yes | ID do projeto. |
| `comparison_start` | body | `date` | no | Data de início da comparação. |
| `comparison_end` | body | `date` | no | Data de fim da comparação. |
