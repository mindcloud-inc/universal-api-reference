# Create Branch with TalentLMS

Creates a new branch in TalentLMS.

## Endpoint

- **Method:** `POST`
- **Path:** `/branches`
- **Base URL:** `https://{domain}.talentlms.com/api/v2`
- **Official documentation:** [Create Branch](https://documenter.getpostman.com/view/31867199/2sAY548Kou#create-a-branch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Branch name. |
| `description` | body | `string` | yes | Branch description. |
| `default_locale` | body | `list` | yes | Branch default locale code. Accepted values: `ar-AE`, `az-AZ`, `bs-BA`, `ca-ES`, `cs-CZ`, `da-DK`, `de-DE`, `el-GR`, `en-US`, `es-ES`, `et-EE`, `fa-IR`, `fi-FI`, `fr-FR`, `he-IL`, `hi-IN`, `hr-HR`, `hu-HU`, `hy-AM`, `id-ID`, `is-IS`, `it-IT`, `ja-JP`, `ka-GE`, `ko-KR`, `lt-LT`, `lv-LV`, `mn-MN`, `ms-MY`, `nb-NO`, `nl-NL`, `pl-PL`, `pt-BR`, `pt-PT`, `ro-RO`, `ru-RU`, `sk-SK`, `sl-SI`, `sr-RS`, `sv-SE`, `th-TH`, `tr-TR`, `uk-UA`, `vi-VN`, `zh-CN`, `zh-TW`. |
