# Plant UML GitBook Plugin

[![Build Status](https://travis-ci.org/vboulaye/gitbook-plugin-local-plantuml-img.svg?branch=master)](https://travis-ci.org/vboulaye/gitbook-plugin-local-plantuml-img)

This plugin builds on the [puml](https://plugins.gitbook.com/plugin/puml) plugin, however this plugin generates the
puml images locally rather than using the service at http://www.plantuml.com/plantuml/.

This is necessary if you are using/hosting gitbook for private work and don't want your diagrams bounced off an external server.

In addition to the standard block plugin call, the plugin processes the img whose src is a .puml file. This allows setting an alt/title attribute and using plugins such as [image-captions](https://github.com/todvora/gitbook-plugin-image-captions) for plantuml generated files.
 
# Release Notes
`1.0.1` Support for caching of output images in the os temp directory. Since the filenames are based on the hash of the diagram text, versioning should 'just work'. This also helps
with the slow-ness listed in issues by only re-rendering changed images. Thanks to @johnhug for the contribution.

# Issues
* Currently a new java process is started for every `plantuml` block in your markdown files. This can be a little slow.
