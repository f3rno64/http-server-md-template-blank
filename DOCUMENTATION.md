## Modules

<dl>
<dt><a href="#module_http-server-md-template-blank">http-server-md-template-blank</a></dt>
<dd><p>Blank template skeleton for <a href="https://github.com/f3rno64/http-server-md">http-server-md</a>, serving as a
reference for the required structure.</p>
<p>Used by the <code>sermit</code> CLI app to create an empty template repo via the
<code>init-template</code> command.</p>
</dd>
</dl>

## Constants

<dl>
<dt><a href="#ASSETS_BUILD_PATH">ASSETS_BUILD_PATH</a></dt>
<dd><p>Artifacts are stored in &amp; resolved from the <code>public/</code> folder within the
project root by default.</p>
</dd>
<dt><a href="#ASSETS">ASSETS</a></dt>
<dd><p>Static asset (files &amp; folders) definition. Sources prefixed with <code>~</code> are
resolved with <code>requireDynamicModule</code>.</p>
<p>{
  &#39;dest/path&#39;: &#39;src/path&#39;
}</p>
</dd>
<dt><a href="#STYLES_BUILD_PATH">STYLES_BUILD_PATH</a></dt>
<dd><p>Artifacts are stored in &amp; resolved from the <code>public/</code> folder within the
project root by default.</p>
</dd>
<dt><a href="#STYLES">STYLES</a></dt>
<dd><p>SCSS style definition, { dest: src }</p>
</dd>
<dt><a href="#NAME">NAME</a></dt>
<dd><p>Unique name to identify template; should form the package name when prefixed
with <code>http-server-md-template-</code>.</p>
</dd>
<dt><a href="#PUBLIC_PATH">PUBLIC_PATH</a></dt>
<dd><p>Absolute path to rendered resources folder, ready for serving.</p>
</dd>
<dt><a href="#INCLUDE_PATH">INCLUDE_PATH</a></dt>
<dd><p>Nunjucks templates are in <code>res/templates</code> within the template root by
default.</p>
</dd>
<dt><a href="#TEMPLATE">TEMPLATE</a></dt>
<dd><p>Recommended filename</p>
</dd>
<dt><a href="#TEMPLATE">TEMPLATE</a></dt>
<dd><p>Recommended filename</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#getConfig">getConfig([userConfig])</a> ⇒ <code>Sermit~Config</code></dt>
<dd><p>Combine the provided &amp; default configurations as-needed.</p>
</dd>
<dt><a href="#genImageMarkdown">genImageMarkdown(params)</a> ⇒ <code>string</code></dt>
<dd><p>Generate a markdown string to display an image at <code>relPath</code>.</p>
</dd>
<dt><a href="#genRawSrcMarkdown">genRawSrcMarkdown(params)</a> ⇒ <code>string</code></dt>
<dd><p>Generate a markdown string to render raw file contents.</p>
</dd>
<dt><a href="#renderPageDirectory">renderPageDirectory(templateConfig)</a> ⇒ <code>Sermit~Renderer</code></dt>
<dd><p>Directory listing renderer.</p>
</dd>
<dt><a href="#renderPageFile">renderPageFile(templateConfig)</a> ⇒ <code>Sermit~FileRenderer</code></dt>
<dd><p>Single file renderer.</p>
</dd>
</dl>

<a name="module_http-server-md-template-blank"></a>

## http-server-md-template-blank
Blank template skeleton for [http-server-md](https://github.com/f3rno64/http-server-md), serving as a
reference for the required structure.

Used by the `sermit` CLI app to create an empty template repo via the
`init-template` command.

**License**: MIT  
<a name="ASSETS_BUILD_PATH"></a>

## ASSETS\_BUILD\_PATH
Artifacts are stored in & resolved from the `public/` folder within the
project root by default.

**Kind**: global constant  
<a name="ASSETS"></a>

## ASSETS
Static asset (files & folders) definition. Sources prefixed with `~` are
resolved with `requireDynamicModule`.

{
  'dest/path': 'src/path'
}

**Kind**: global constant  
<a name="STYLES_BUILD_PATH"></a>

## STYLES\_BUILD\_PATH
Artifacts are stored in & resolved from the `public/` folder within the
project root by default.

**Kind**: global constant  
<a name="STYLES"></a>

## STYLES
SCSS style definition, { dest: src }

**Kind**: global constant  
<a name="NAME"></a>

## NAME
Unique name to identify template; should form the package name when prefixed
with `http-server-md-template-`.

**Kind**: global constant  
<a name="PUBLIC_PATH"></a>

## PUBLIC\_PATH
Absolute path to rendered resources folder, ready for serving.

**Kind**: global constant  
<a name="INCLUDE_PATH"></a>

## INCLUDE\_PATH
Nunjucks templates are in `res/templates` within the template root by
default.

**Kind**: global constant  
<a name="TEMPLATE"></a>

## TEMPLATE
Recommended filename

**Kind**: global constant  
<a name="TEMPLATE"></a>

## TEMPLATE
Recommended filename

**Kind**: global constant  
<a name="getConfig"></a>

## getConfig([userConfig]) ⇒ <code>Sermit~Config</code>
Combine the provided & default configurations as-needed.

**Kind**: global function  
**Returns**: <code>Sermit~Config</code> - config  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| [userConfig] | <code>Sermit~Config</code> | <code>{}</code> | provided configuration |

<a name="genImageMarkdown"></a>

## genImageMarkdown(params) ⇒ <code>string</code>
Generate a markdown string to display an image at `relPath`.

**Kind**: global function  
**Returns**: <code>string</code> - md  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>object</code> | params |
| params.relPath | <code>string</code> | path relative to content root path. |
| params.name | <code>string</code> | image alt text. |

<a name="genRawSrcMarkdown"></a>

## genRawSrcMarkdown(params) ⇒ <code>string</code>
Generate a markdown string to render raw file contents.

**Kind**: global function  
**Returns**: <code>string</code> - md  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>object</code> | params |
| params.srcPath | <code>string</code> | path to file, resolvable locally via `fs` |

<a name="renderPageDirectory"></a>

## renderPageDirectory(templateConfig) ⇒ <code>Sermit~Renderer</code>
Directory listing renderer.

**Kind**: global function  
**Returns**: <code>Sermit~Renderer</code> - renderer  

| Param | Type | Description |
| --- | --- | --- |
| templateConfig | [<code>Config</code>](#SermitBlankTemplate..Config) | template config data. |

<a name="renderPageFile"></a>

## renderPageFile(templateConfig) ⇒ <code>Sermit~FileRenderer</code>
Single file renderer.

**Kind**: global function  
**Returns**: <code>Sermit~FileRenderer</code> - renderer  

| Param | Type | Description |
| --- | --- | --- |
| templateConfig | [<code>Config</code>](#SermitBlankTemplate..Config) | template config data. |

