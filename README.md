# yeogurt-dashboard-example

An example of how to create a site dashboard within the [Yeogurt](https://github.com/larsonjj/generator-yeogurt) generator.

> NOTE: Only Jade is supported currently. Nunjucks support will be coming soon!

## Usage

Copy files into a yeogurt generated project using cURL:

```
# Run this inside the root of your Yeogurt generated project
curl -L https://github.com/larsonjj/yeogurt-dashboard-example/tarball/master | tar -xzv --strip-components 1 --exclude={README.md,LICENSE.md}
```

This will add the needed files to your project.

## Data

The JSON files generated in the `_data/dashboard` folder will be parsed and added to your template engine (i.e. Jade).
The data will look like the following:

```js
{
  dashboard: {
    header: {
      name: 'Header',
      link: '/dashboard/modules/header.html',
      category: 'Module',
      status: 'InProgress'
    },
    index: {
      name: 'Home',
      link: '/',
      category: 'Page',
      status: 'InProgress'
    },
    statuses: [ [Object], [Object], [Object], [Object], [Object] ]
  }
}
```

### Statuses data

You can update the available statuses and their associated text/bg colors within the `_data/dashboard/statuses.json`.
The data looks like the following:

```js
{
  "name": "InProgress"
  "color": "#fff",
  "bgcolor": "#94caeb"
}
```

## License

[MIT License](LICENSE.md) - &copy; Jake Larson
