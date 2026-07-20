# Create Report with Reportei

Creates a new report in Reportei.

## Endpoint

- **Method:** `POST`
- **Path:** `/reports`
- **Base URL:** `https://app.reportei.com/api/v2`
- **Official documentation:** [Create Report](https://developers.reportei.com#relatorios-endpoint-2)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Título do relatório. |
| `subtitle` | body | `string` | yes | Legenda do relatório. |
| `start` | body | `date` | yes | Data de início da análise. |
| `end` | body | `date` | yes | Data de fim da análise. |
| `template_id` | body | `number` | yes | ID do template. |
| `integration_ids[]` | body | `array<number>` | yes | Array de IDs das integrações selecionadas. |
| `project_id` | body | `number` | yes | ID do projeto. |
| `comparison_start` | body | `date` | no | Data de início da comparação. |
| `comparison_end` | body | `date` | no | Data de fim da comparação. |
