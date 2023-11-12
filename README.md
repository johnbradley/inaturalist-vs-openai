# iNaturalist vs OpenAI
[Butterfly-GPT-4V-Test notebook](Butterfly-GPT-4V-Test.ipynb) compares species names determined by the [OpenAI gpt-4-vision-preview model](https://platform.openai.com/docs/guides/vision) against data from [iNaturalist](https://www.inaturalist.org/). 
The notebook fetches observations (images) from iNaturalist by fetching 10 images for two species names: 'Heliconius melpomene' and 'Heliconius erato'.
The images are used with the OpenAI API and a prompt to determine a species name for each observation.

## Results
The complete results are visible in the notebook.
The OpenAI results seem pretty good, but were not consistent between runs.
This inconsistency is expected since the notebook uses the default OpenAI `temperature`.



## Preview Model Limitations
The model being used is a preview so only 100 requests are allwed per day.
When this limit is exceeded the following error occurs:
```
RateLimitError: Error code: 429 - {'error': {
  'message': 'Rate limit reached for gpt-4-vision-preview in ... on requests per day (RPD): Limit 100,...}}                                          
```
