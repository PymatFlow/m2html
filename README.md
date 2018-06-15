# m2html
Documentation Generator for Matlab M-files and Toolboxes in HTML

M2HTML by itself generates an HTML documentation of the Matlab M-files found
 in the direct subdirectories of the current directory. HTML files are 
 written in a 'doc' directory (created if necessary). All the others options
 are set to default (in brackets in the following).
 
 M2HTML('PropertyName1',PropertyValue1,'PropertyName2',PropertyValue2,...)
 sets multiple option values. The list of option names and default values is:
 o mFiles - Cell array of strings or character array containing the
 list of M-files and/or directories of M-files for which an HTML
 documentation will be built (use relative paths without backtracking).
 Launch M2HTML one directory above the directory your wanting to
 generate documentation for [ <all direct subdirectories> ]
 
* htmlDir - Top level directory for generated HTML files [ 'doc' ]
* recursive - Process subdirectories recursively [ on | {off} ]
* source - Include Matlab source code in the generated documentation  [ {on} | off ]
* download - Add a link to download each M-file separately [ on | {off} ]
* syntaxHighlighting - Source Code Syntax Highlighting [ {on} | off ]
* tabs - Replace '\t' (horizontal tab) in source code by n white space  characters [ 0 ... {4} ... n ]
* globalHypertextLinks - Hypertext links among separate Matlab  directories [ on | {off} ]
* todo - Create a TODO list in each directory summarizing all the  ' TODO ' lines found in Matlab code [ on | {off}]
* graph - Compute a dependency graph using GraphViz [ on | {off}]  'dot' required, see <http://www.graphviz.org/>
* indexFile - Basename of the HTML index file [ 'index' ]
* extension - Extension of generated HTML files [ '.html' ]
* template - HTML template name to use [ {'blue'} | 'frame' | ... ]
* search - Add a PHP search engine [ on | {off}] - beta version!
* save - Save current state after M-files parsing in 'm2html.mat'  in directory htmlDir [ on | {off}]
* load - Load a previously saved '.mat' M2HTML state to generate HTML  files once again with possibly other options [ <none> ]
* verbose - Verbose mode [ {on} | off ]

 For more information, please read the M2HTML tutorial and FAQ at:
 <http://www.artefact.tk/software/matlab/m2html/>

 Examples:
 ```
 >> m2html('mfiles','matlab', 'htmldir','doc');
 
 >> m2html('mfiles',{'matlab/signal' 'matlab/image'}, 'htmldir','doc');
 
 >> m2html('mfiles','matlab', 'htmldir','doc', 'recursive','on');
 
 >> m2html('mfiles','mytoolbox', 'htmldir','doc', 'source','off');
 
 >> m2html('mfiles','matlab', 'htmldir','doc', 'global','on');
 
 >> m2html( ... , 'template','frame', 'index','menu');
 ```

