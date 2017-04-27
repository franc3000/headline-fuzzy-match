# headline-fuzzy-match
fuzzy matching of headlines to identify unique strings

The purpose of this code is to take an array of strings, and determine which ones are highly similar.

Sample input data:

```json
{
  "titles": [
    "Hong Kong under tight security for Chinese official's visit | Daily Mail Online",
    "Hong Kong under tight security for Chinese official's visit",
    "Hong Kong ups security for Chinese official - Taipei Times",
    "Hong Kongâs pro-democracy groups drape banners from hills as Zhang Dejiang arrives | South China Morning Post",
    "It was not a good day to be a drone in Hong Kong - LA Times",
    "Joshua Wong convicted for democracy protests in Hong Kong | The Week UK",
    "Massive security operation shuts down protest in Hong Kong as top Chinese official visits | KBIA",
    "Massive security operation shuts down protest in Hong Kong as top Chinese official visits | Public Radio International"
  ]
}
```

Output data (example, not exact):

```json
{
  "titles": [
    {
      "fuzzy_match_titles": [
        "Hong Kong under tight security for Chinese official's visit | Daily Mail Online",
        "Hong Kong under tight security for Chinese official's visit",
        "Hong Kong ups security for Chinese official - Taipei Times"
      ],
      "main_title": "Hong Kong under tight security for Chinese official's visit | Daily Mail Online"
    },
    {
      "fuzzy_match_titles": [
        "Massive security operation shuts down protest in Hong Kong as top Chinese official visits | Public Radio International"
      ],
      "main_title": "Massive security operation shuts down protest in Hong Kong as top Chinese official visits | KBIA"
    },
    ...
  ]
}
```
