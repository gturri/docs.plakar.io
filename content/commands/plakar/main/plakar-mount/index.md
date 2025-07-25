---
date: "2025-07-15T19:14:54Z"
title: plakar-mount
summary: "Mount Plakar snapshots as read-only filesystem"
---
<div class="head" role="doc-pageheader" aria-label="Manual header
  line"><span class="head-ltitle">PLAKAR-MOUNT(1)</span>
  <span class="head-vol">General Commands Manual</span>
  <span class="head-rtitle">PLAKAR-MOUNT(1)</span></div>
<main class="manual-text">
<section class="Sh">
<h2 class="Sh" id="NAME"><a class="permalink" href="#NAME">NAME</a></h2>
<p class="Pp"><code class="Nm">plakar-mount</code> &#x2014;
    <span class="Nd" role="doc-subtitle">Mount Plakar snapshots as read-only
    filesystem</span></p>
</section>
<section class="Sh">
<h2 class="Sh" id="SYNOPSIS"><a class="permalink" href="#SYNOPSIS">SYNOPSIS</a></h2>
<table class="Nm">
  <tr>
    <td><code class="Nm">plakar mount</code></td>
    <td><var class="Ar">mountpoint</var></td>
  </tr>
</table>
</section>
<section class="Sh">
<h2 class="Sh" id="DESCRIPTION"><a class="permalink" href="#DESCRIPTION">DESCRIPTION</a></h2>
<p class="Pp">The <code class="Nm">plakar mount</code> command mounts a Plakar
    repository snapshot as a read-only filesystem at the specified
    <var class="Ar">mountpoint</var>. This allows users to access snapshot
    contents as if they were part of the local file system, providing easy
    browsing and retrieval of files without needing to explicitly restore them.
    This command may not work on all Operating Systems.</p>
</section>
<section class="Sh">
<h2 class="Sh" id="EXAMPLES"><a class="permalink" href="#EXAMPLES">EXAMPLES</a></h2>
<p class="Pp">Mount a snapshot to the specified directory:</p>
<div class="Bd Pp Bd-indent Li">
<pre>$ plakar mount ~/mnt</pre>
</div>
</section>
<section class="Sh">
<h2 class="Sh" id="DIAGNOSTICS"><a class="permalink" href="#DIAGNOSTICS">DIAGNOSTICS</a></h2>
<p class="Pp">The <code class="Nm">plakar-mount</code> utility exits&#x00A0;0 on
    success, and&#x00A0;&gt;0 if an error occurs.</p>
<dl class="Bl-tag">
  <dt>0</dt>
  <dd>Command completed successfully.</dd>
  <dt>&gt;0</dt>
  <dd>An error occurred, such as an invalid mountpoint or failure during the
      mounting process.</dd>
</dl>
</section>
<section class="Sh">
<h2 class="Sh" id="SEE_ALSO"><a class="permalink" href="#SEE_ALSO">SEE
  ALSO</a></h2>
<p class="Pp"><a class="Xr" href="../plakar/" aria-label="plakar, section
    1">plakar(1)</a></p>
</section>
</main>
<div class="foot" role="doc-pagefooter" aria-label="Manual footer
  line"><span class="foot-left">Plakar</span> <span class="foot-date">July 3,
  2025</span> <span class="foot-right">PLAKAR-MOUNT(1)</span></div>
