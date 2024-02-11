# BJ Location Data


Benin Republic location data for web and mobile apps

For mobile (dart/flutter) version, please visit [location_data_bj](https://pub.dev/packages/location_data_bj) dart package

For javascript version, please visit [location_data_bj](https://www.npmjs.com/package/location_data_bj) npm package

>
>
> Data Snapshot (As of 2023-12-21)
>
> Department: 12
>
> Town: 77
>
> District: 546
>
> Neighborhood: 5303
>
------------------------


## Replacing `id` with `code` within library

To ease the use of this dataset, the `id` field has been replaced with `code` field. 

This field has no impact on the data itself. It is only used to facilitate the use of the data.

## What logic was used to generate the `code` field?

It implements the `generateCode` function which is used to generate codes based on the following principle:

1. Eliminate duplicates in the data.
2. Sort objects in the list alphabetically by the "name" key.
3. Codes are generated by taking the first three letters of each key.
4. If codes are identical:
    - The first occurrence is kept.
    - From the second to the last occurrence of the repetition, for each one, the next letter is taken to form a new three-letter code.
    Example: "abomey", "abomey-calavi"...
    Results: "abo", "abm"

    - If the key runs out of letters, a rising digit is added to form a new three-letter code.
    Example: "zou" and "zous" might result in "zo1" and "zo2" respectively.



## Disclaimer
Please note that the dataset used is not official. It is based on the work done by [Junior Gantin](https://github.com/nioperas06) at [this repos](https://github.com/nioperas06/bj-decoupage-territorial).


## License
Bj Location Data is crafted with ❤️ by [Dah-Kenangnon Justin](https://dah-kenangnon.com) and is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

These person has helped me for cleaning the data and making it easier to use in dart and javascript:

- Big thanks to [Jude AGBODOYETIN](https://github.com/Jude200)
- Big thanks to [Yanel Aïna](https://github.com/yanelaina)
