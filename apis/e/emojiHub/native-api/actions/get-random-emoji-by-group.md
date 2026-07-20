# Get Random Emoji By Group with EmojiHub

Retrieves a random emoji from a selected EmojiHub group.

## Endpoint

- **Method:** `GET`
- **Path:** `/random/group/:group`
- **Base URL:** `https://emojihub.yurace.pro/api`
- **Official documentation:** [Get Random Emoji By Group](https://github.com/cheatsnake/emojihub)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group` | path | `list<string>` | yes | Emoji group in kebab-case format. Accepted values: `activities`, `animal-amphibian`, `animal-bird`, `animal-bug`, `animal-mammal`, `animal-marine`, `animal-reptile`, `body`, `cat-face`, `clothing`, `creature-face`, `dishware`, `drink`, `emotion`, `face-negative`, `face-neutral`, `face-positive`, `face-role`, `face-sick`, `family`, `flags`, `food-asian`, `food-fruit`, `food-prepared`, `food-sweet`, `food-vegetable`, `monkey-face`, `objects`, `person`, `person-activity`, `person-gesture`, `person-role`, `plant-flower`, `plant-other`, `skin-tone`, `symbols`, `travel-and-places`. |
