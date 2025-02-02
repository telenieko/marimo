# Deploying

```{eval-rst}
.. toctree::
  :maxdepth: 2
  :hidden:

  programmatically
  deploying_docker
  deploying_public_gallery
  deploying_marimo_cloud
  deploying_ploomber
  deploying_railway
  prebuilt_containers
  authentication
```

These guides help you deploy marimo notebooks.

|                                 |                                                           |
| :------------------------------ | :-------------------------------------------------------- |
| {doc}`programmatically`         | Programmatically run the marimo backend for customization |
| {doc}`deploying_docker`         | Deploy with Docker                                        |
| {doc}`deploying_public_gallery` | Deploy our public gallery                                 |
| {doc}`deploying_marimo_cloud`   | Deploy to Marimo Cloud                                    |
| {doc}`deploying_ploomber`       | Deploy to Ploomber Cloud                                  |
| {doc}`deploying_railway`        | Deploy to Railway                                         |
| {doc}`prebuilt_containers`      | Prebuilt containers                                       |
| {doc}`authentication`           | Authentication and security                               |

```{admonition} Sharing notebooks on the public web
:class: tip

To share notebooks on the public web, try using [WASM
notebooks](../../guides/wasm.md), an implementation of marimo that runs
entirely in the browser -- no backend required.

WASM notebooks support most but not all Python features and packages. See our
[guide on WASM notebooks](../../guides/wasm.md) to learn more.
```

```{admonition} Marimo Cloud
:class: tip

For a turnkey cloud solution, try [Marimo Cloud](/guides/deploying/deploying_marimo_cloud.md).
```

## Programmatically running the marimo backend

When deploying marimo notebooks, you can run the marimo backend programmatically. This allows you to customize the backend to your needs and deploy it in your own environment.

See the [programmatically running the marimo backend guide](programmatically.md) for more information.

## Health and status endpoints

The following endpoints may be useful when deploying your application:

- `/health` - A health check endpoint that returns a 200 status code if the application is running as expected
- `/healthz` - Same as above, just a different name for easier integration with cloud providers
- `/api/status` - A status endpoint that returns a JSON object with the status of the server

## Configuration

If you would like to deploy your application at a subpath, you can set the `--base-url` flag when running your application.

```bash
marimo run app.py --base-url /subpath
```

## Including code in your application

You can include code in your application by using the `--include-code` flag when running your application.

```bash
marimo run app.py --include-code
```
