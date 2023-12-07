# Microsoft Developer Platform Providers

`// TODO`

## Providers

| Repo                                                         | Description                                                  |                                                                                                                                                                                                   |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [developer-platform-github][developer-platform-github]       | The GitHub provider(s)                                       | [![developer-platform-github](https://img.shields.io/github/v/release/microsoft/developer-platform-github?logo=github)](https://github.com/microsoft/developer-platform-github/releases)          |
| [developer-platform-devcenter][developer-platform-devcenter] | The Dev Center [Azure Deployment Environments][ade] provider | [![developer-platform-devcenter](https://img.shields.io/github/v/release/microsoft/developer-platform-devcenter?logo=github)](https://github.com/microsoft/developer-platform-devcenter/releases) |

## nuget.config

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <!--To inherit the global NuGet package sources remove the <clear/> line below -->
    <clear />
    <add key="nuget" value="https://api.nuget.org/v3/index.json" />
    <add key="msdev" value="https://msdevnuget.blob.core.windows.net/feed/index.json" />
  </packageSources>

  <!-- Microsoft.Developer.* packages will be restored from msdev, everything else from nuget.org. -->
  <packageSourceMapping>
    <packageSource key="nuget">
      <package pattern="*" />
    </packageSource>
    <packageSource key="msdev">
      <package pattern="Microsoft.Developer.*" />
    </packageSource>
  </packageSourceMapping>
</configuration>
```

## Contributing

This project welcomes contributions and suggestions. Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.

[developer-platform-devcenter]: https://github.com/microsoft/developer-platform-devcenter
[developer-platform-github]: https://github.com/microsoft/developer-platform-github
[ade]: https://azure.microsoft.com/en-us/products/deployment-environments
