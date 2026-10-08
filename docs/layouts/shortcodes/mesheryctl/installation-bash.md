
To install or upgrade `mesheryctl` using `bash`, execute anyone of the following commands.

#### Option 1: Only install `mesheryctl` binary

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | DEPLOY_MESHERY=false bash -
 </div></div>
 </pre>
<br />
<br />

#### Option 2: Install `mesheryctl` binary and deploy Meshery on Docker

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | PLATFORM=docker bash -
 </div></div>
 </pre>
<br />
<br />

#### Option 3: Install `mesheryctl` binary and deploy Meshery on Kubernetes

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | PLATFORM=kubernetes bash -
 </div></div>
 </pre>
<br />
<br />

#### Option 4: Install `mesheryctl` binary and Meshery adapter(s)

Install `mesheryctl` binary and include one or more [adapters]({{ relref . "concepts/architecture/adapters.md" }}) to be deployed

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | ADAPTERS=consul PLATFORM=kubernetes bash -
 </div></div>
 </pre>
<br />
<br />

### Start Meshery
You are ready to deploy Meshery `mesheryctl`. To do so, execute the following command.

 <pre class="codeblock-pre"><div class="codeblock">
 <div class="clipboardjs">mesheryctl system start</div></div>
 </pre>

If you are running Meshery on Docker, execute the following command.

 <pre class="codeblock-pre"><div class="codeblock">
 <div class="clipboardjs">mesheryctl system start -p docker</div></div>
 </pre>

### Uninstall `mesheryctl` using Bash

To uninstall `mesheryctl`, execute the following command.

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | bash -s -- --uninstall
 </div></div>
 </pre>

The uninstall script displays a warning prompt asking for confirmation (`yes/no`). To skip this confirmation, pass the `--yes` flag:

 <pre class="codeblock-pre">
 <div class="codeblock">
 <div class="clipboardjs">
  $ curl -L https://meshery.io/install | bash -s -- --uninstall --yes
 </div></div>
 </pre>

*Note: The uninstall script only removes the `mesheryctl` binary; user configuration under `~/.meshery` is preserved.*

