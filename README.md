Examples data registry and tooling

## Registry

Registry is maintained as [Tabular Data Package][tdp] with list of datasets in examples-list.csv.

[tdp]: http://frictionlessdata.io/guides/tabular-data-package/

To add a dataset add it to the `examples-list.csv`.

Discussion of proposals for new datasets and for incorporation of prepared datasets takes place in the [issues][].

To **propose a new dataset for inclusion**, please create a [new issue](https://github.com/datasets/registry/issues/new).

[issues]: https://github.com/datasets/registry/issues

## Examples Dataset Tools

In order to use tools, please use index.js in Core registry https://github.com/datasets/registry

### Installation

``` 
$ npm install
```

### Usage

* Environmental variables

`DOMAIN` - testing or production environment. For example: https://datahub.io
`TYPE` - type of dataset. For example: examples or core

```
node index.js [COMMAND] [PATH]
# PATH - path to csv file
```

#### Clone datasets

To clone all examples datasets run the following command:

`npm index.js clone [PATH]`

It will clone all examples datasets into following directory: `data/${pkg_name}`

#### Check datasets

To check all examples datasets run the following command:

`npm index.js check [PATH]`

It will validate metadata and data according to the latest spec. 

#### Normalize datasets

To normalize all examples datasets run the following command:

`npm index.js norm [PATH]`

It will normalize all examples datasets in the following directory: `data/${pkg_name}`

#### Push datasets

To publish all examples data packages run the following command:

`npm index.js push [PATH]`

### Running tests

We use Ava for our tests. For running tests use:

```
$ [sudo] npm test
```

To run tests in watch mode:

```
$ [sudo] npm run watch:test
```
