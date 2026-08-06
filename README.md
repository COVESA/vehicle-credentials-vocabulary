## Verifiable Vehicle Credentials

This specification describes a data model for use when securing vehicle credentials using
[Verifiable Credentials](https://www.w3.org/TR/vc-data-model-2.0/).

The `vocabulary.yml` document in this repo is intended to be used with the
[yml2vocab](https://github.com/w3c/yml2vocab?tab=readme-ov-file) tool from
the W3C.

### Discussion Forums
* [W3C Credentials Community Group Mailing List (Incubation)](https://lists.w3.org/Archives/Public/public-credentials/)
* [W3C Verifiable Credentials WG Mailing List (Standardization)](https://lists.w3.org/Archives/Public/public-vc-wg/)

### Other Relevant Verifiable Credential Working Group Repositories
* [Use Cases](https://www.w3.org/TR/vc-use-cases/)
* [Data Model](https://www.w3.org/TR/vc-data-model-2.0/)
* [Data Integrity](https://www.w3.org/TR/vc-data-integrity/)

## Usage

Run the following to generate the ontology description in HTML, JSON-LD,
and Turtle (`.ttl`).

```sh
npm run build
```

The output will result in...
* `dist/index.html` - the Ontology in HTML and usage documentation
* `dist/vocabulary.context.jsonld` - the latest JSON-LD context file
* `vocabulary.jsonld` - the Ontology in JSON-LD
* `vocabulary.ttl` - the Ontology in Turtle

The Ontology files can be used by modeling tools as needed. Additionally, the
JSON-LD context file can be used during testing.

## Releasing

Once the vocabulary/ontology and context file are ready for more permanence, the
following command can be used to create a release:

```sh
$ npm run release -- v1rc1
```

This will result in a `dist/contexts/v1rc1.jsonld` file.
