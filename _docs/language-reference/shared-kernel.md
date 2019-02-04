---
title: Shared Kernel
permalink: /docs/shared-kernel/
---

The Shared Kernel pattern describes a relationship between two bounded contexts and is used on a [context map](/docs/context-map/) in CML.

## Syntax
Note that currently two different syntax variants exist. The following code snippets illustrate both variants:

<div class="highlight"><pre><span></span>CargoBookingContext &lt;-&gt; VoyagePlanningContext : <span class="k">Shared-Kernel</span> {
  <span class="k">implementationTechnology</span> = <span class="s">&quot;Java Library&quot;</span>
}
</pre></div>

Note that with this syntax (with the arrows _&lt;-&gt;_) it does not matter which bounded context is on which side, since this is a symmetric relationship. If you switch the bounded contexts, it has the same meaning semantically.

<div class="highlight"><pre><span></span>CargoBookingContext <span class="k">Shared-Kernel</span> VoyagePlanningContext {
  <span class="k">implementationTechnology</span> = <span class="s">&quot;Java Library&quot;</span>
}
</pre></div>

### Implementation Technology
With the _implementationTechnology_ keyword you can specify how the relationship is implemented.

### Relationship Name
With an _@_ it is possible to annotate every relationship on a context map a name, as illustrated within this example:

<div class="highlight"><pre><span></span>@BookingVoyageRelationship
CargoBookingContext <span class="k">Shared-Kernel</span> VoyagePlanningContext {
  <span class="k">implementationTechnology</span> = <span class="s">&quot;Java Library&quot;</span>
}
</pre></div>
