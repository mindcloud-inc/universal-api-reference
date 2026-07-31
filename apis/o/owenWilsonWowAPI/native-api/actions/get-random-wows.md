# Get Random Wows with Owen Wilson Wow API

## Endpoint

- **Method:** `GET`
- **Path:** `/wows/random`
- **Base URL:** `https://owen-wilson-wow-api.onrender.com`
- **Official documentation:** [Get Random Wows](https://github.com/amamenko/owen-wilson-wow-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `results` | query | `number` | no | Number of random wow results to retrieve. |
| `year` | query | `number` | no | Return a random wow from this year. |
| `movie` | query | `string` | no | Return a random wow from this movie. |
| `director` | query | `string` | no | Return a random wow from this director. |
| `wow_in_movie` | query | `number` | no | Return a random wow by its occurrence number in the movie. |
| `sort` | query | `string` | no | Sort multiple random results by movie, release_date, year, director, or number_current_wow. |
| `direction` | query | `string` | no | Sort direction: asc or desc. |
