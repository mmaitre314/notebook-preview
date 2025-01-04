> WIP

# Notebook Preview

An Azure DevOps (ADO) extension to preview notebooks.

## References

- List of content renderers in ADO Marketplace: https://github.com/search?q=repo%3Arenovatebot%2Fazure-devops-marketplace%20ms.vss-code-web.content-renderer&type=code
- A few ADO content renderers:
	- https://github.com/Microsoft/vsts-extension-samples/blob/master/custom-content-renderer/vss-extension.json
    - https://github.com/xinyi-joffre/azure-devops-mermaid-renderer/blob/main/vss-extension.json
	- https://github.com/Azure/ipynb-renderer/blob/master/vss-extension.json
- Server-side handling of content renderers? https://github.com/azure-devops-extensions/azure-devops-server-controls/blob/cfbda8414392caefa74433f760d21bfcbd23c723/_static/tfs/Dev17.M153.5/_scripts/TFS/debug/Presentation/Scripts/TFS/TFS.ContentRendering.ts#L157
- Jupyter notebook viewers:
  - https://jupyterlite.readthedocs.io/en/latest/
  - https://github.com/gzuidhof/starboard-notebook
  - https://nbdime.readthedocs.io/en/latest/