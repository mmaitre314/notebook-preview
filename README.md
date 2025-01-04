> WIP

# Notebook Preview

An Azure DevOps (ADO) extension to preview notebooks.

## Design Ideas

Potential entry points:
- `ms.vss-code-web.source-item-menu`
  - For Azure Synapse notebooks, may be able to limit handling of JSON files to paths matching glob `**/notebook/*.json`.
  - Preview by popping a side panel? Concern: limited screen space.
  - ADO code sample: https://github.com/microsoft/azure-devops-extension-sample/tree/master/src/Samples/source-item-menu
- `ms.vss-code-web.pull-request-action-menu`
  - ADO code sample: https://github.com/microsoft/azure-devops-extension-sample/tree/master/src/Samples/pull-request-action-menu
- `ms.vss-code-web.content-renderer`
  - Concerns: may conflict with `ipynb-renderer` on `.ipynb` file extension. Also, Synapse Notebook file extension `.json` is too generic to handle.

For code diff, see [Myers Algorithm](http://www.xmailserver.org/diff2.pdf) both within and across notebook cells.
Within cells, see [Monaco Diff Editor](https://microsoft.github.io/monaco-editor/docs.html#functions/editor.createDiffEditor.html).

## References

- List of content renderers in ADO Marketplace: https://github.com/search?q=repo%3Arenovatebot%2Fazure-devops-marketplace%20ms.vss-code-web.content-renderer&type=code
- A few ADO content renderers
	- https://github.com/Microsoft/vsts-extension-samples/blob/master/custom-content-renderer/vss-extension.json
    - https://github.com/xinyi-joffre/azure-devops-mermaid-renderer/blob/main/vss-extension.json
	- https://github.com/Azure/ipynb-renderer/blob/master/vss-extension.json
- Server-side handling of content renderers? https://github.com/azure-devops-extensions/azure-devops-server-controls/blob/cfbda8414392caefa74433f760d21bfcbd23c723/_static/tfs/Dev17.M153.5/_scripts/TFS/debug/Presentation/Scripts/TFS/TFS.ContentRendering.ts#L157
- ADO docs
  - https://github.com/microsoft/azure-devops-extension-sample
  - https://docs.microsoft.com/en-us/azure/devops/extend/overview?view=vsts
  - https://learn.microsoft.com/en-us/azure/devops/extend/get-started/node?view=azure-devops
  - https://marketplace.visualstudio.com/azuredevops
  - https://learn.microsoft.com/en-us/azure/devops/extend/develop/samples-overview?view=azure-devops
  - https://developer.microsoft.com/en-us/azure-devops/develop/extensions
- Jupyter notebook viewers
  - https://jupyterlite.readthedocs.io/en/latest/
  - https://github.com/gzuidhof/starboard-notebook
  - https://nbdime.readthedocs.io/en/latest/
- Monaco:
  - https://github.com/microsoft/monaco-editor
- GitHub notebook preview
  - https://github.blog/changelog/2023-03-01-feature-preview-rich-jupyter-notebook-diffs/
- Feature requests
  - https://developercommunity.visualstudio.com/t/Need-better-rich-text-diff-for-notebooks/10617374