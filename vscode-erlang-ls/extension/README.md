# erlang-ls/vscode

The erlang-ls extension for VSCode.

## Available Features

### Code Completion

Get context-aware code completions for function names, macros,
records, variable names and more.

![Code Completion](https://github.com/erlang-ls/docs/raw/master/png/vscode/01-code-completion.png)

### Go To Definition

Navigate to the definition of a function, macro, record or type.

### Go To Implementation for OTP Behaviours

Hovering a `gen_server:start_link` call? Jump to the respective `init`
function with a single keystroke.

### Signature Suggestions

Never remember the order of the `lists:keytake/3` function? You are
not alone. We got you covered.

### Compiler Diagnostics

Display warnings and errors from the compiler inline.

![Compiler Diagnostics](https://github.com/erlang-ls/docs/raw/master/png/vscode/05-compiler-diagnostics.png)

### Dialyzer Diagnostics

It has never been so easy to make Dialyzer happy.

### Elvis Diagnostics

Display [Elvis](https://github.com/inaka/elvis) style suggestions
inline. No more nit-picking comments from colleagues!

### Edoc

Hover a local or remote function to see its `edoc`. You will miss this
feature so much when edocs are not available that you will start
writing them!

### Navigation for Included Files

Navigate to included files with a single click.

### Find/Peek References

Who is calling this function? Figure it out without leaving the
current context.

![Peek References](https://github.com/erlang-ls/docs/raw/master/png/vscode/11-peek-references.png)

### Outline

Get a nice outline of your module on the side and jump between
functions.

![Outline](https://github.com/erlang-ls/docs/raw/master/png/vscode/12-outline.png)

### Workspace Symbols

Jump to the module you're looking for, in no time.

### Folding

Focus on what's important, fold the rest.

## Changelog

### 0.0.11

Extension:

- Include .escript among known file extensions

Server:

- Improve URI handling
- Introduce support for code lenses
- Introduce server-info code lense (disabled by default)
- Fix some Windows incompatibilities
- Avoid the entire server crashing in case of failing providers
- Improve support for Unicode
- Introduce background jobs
- Show progress while indexing
- Fix handling of empty RootUri (Sublime users should enjoy this)
- Add support for .escript files
- Update logging framework
- Add support for finding type references
- Enable logging by default
- Remove eflame dependency
- Add auto-completion for built-in functions and types
- Goto definition on an atom goes to that module if it exists
- Fix symlinks handling
- Add auto-completion for atoms
- Add edoc support for OTP modules (requires OTP 23 once available)
- Introduce CLI help menu via getopt

### 0.0.10

Extension:

- Configurable log level (default: none)
- Configurable log path

Server:

- Add auto completion for types in `spec` and `export_types` contexts
- Fix Elvis diagnostics for modules not belonging to the workspace
- Fix off-by-one folding ranges for some editors
- Restrict dependencies from accessing stdio, avoiding crashes on hover
- Speed up indexing
- Add syntax-highlighting for hover information
- Fix inclusion path for dependencies
- Show function information when hovering the `export` list
- Add plumbing for code lenses
- Find module references
- Find macro references
- Update code formatter to latest available version
- Fix ranges for Dialyzer diagnostics
- Avoid crash in presence of : within strings
- Fix supervision strategy
- Avoid un-necessary parsing
- Asynchronous diagnostics

### 0.0.9

Server:

- Add support for behaviours diagnostics (compiler, dialyzer)
- Add support for parse transform (compiler)
- Find references for records
- Fix support for `$/` notifications and requests
- Be able to specify a different location for the `erlang_ls.config` file
- Fix issue with Elvis diagnostics polluting stdio
- Add root uri to start-up message
- Fix include_dirs passed to Dialyzer
- Inject exit message when TCP socket is closed
- Add support for custom macros
- Add support for hot-code reloading

### 0.0.8

Extension:

- Fix support for Windows
- Add option to override the path to the language server

### 0.0.7

Extension:

- Add list of features to README
- Enable debug mode

### 0.0.6

Extension:

- Bump vscode-languageclient to 6.0.0

Server:

- Add navigation to callback functions for OTP behaviours
- Add support for folding ranges
- Allow a system-wide erlang_ls.config file
- Show edoc for local functions
- Support cancel requests
- Fix support for Dialyzer diagnostics
- Show errors from included .hrl files
- Correctly handle macros on record access
- Remove dependency on wx
- Use platform-dependent log directories
- Automatically generate diagnostics when opening a file
- Limit the amount of symbols returned as workspace symbols
- Add plumbing for a formatter
- Add support for umbrella projects
- Add code completion for record fields
- Use a persistent database (Mnesia) to store indexed information
- Add support for Elvis diagnostics
- Handle multiple export sections
- Do not crash on un-handled extensions
- Do not crash when macros are used as function names
- Other bug fixes and stability improvements

### 0.0.5

Extension:

- Ignore TextMate folders that are not used by the extension
- Add language configuration, including comments and brackets

Server:

- Report server version on startup
- Fix ranges for compiler diagnostics
- Fix completion of function/arity in export lists
- Introduce document highlighting
- Improve performance of workspace symbol lookups
- Add completion for record names
- Improve indexing performances
- Properly cleanup outdated references
- Other bug fixes and stability improvements

### 0.0.4

Extension:

- Do not include un-necessary files in the package, reducing the
  extension size from 20MB to 15MB

### 0.0.3

Extension:

- Add configuration option to enable tracing calls between client and server

### 0.0.2

Server:

- Performance improvements for the indexing process
- Add code navigation for opaque types
- Fix issue with non-unicode modules
- Skip indexing of some OTP applications by default (diameter, megaco, snmp, wx)
- Fix support for Markdown content on hover requests

### 0.0.1

Initial version of the extension.
