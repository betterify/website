<script context="module">
  export const prerender = true;
</script>

<script>
  import { testimonials } from "$lib/contents/home/index";
  import {
    features,
    otherFeatures,
    secondaryFeatures as cards,
  } from "$lib/contents/home/features";

  import Features from "$lib/components/features.svelte";
  import ChooseProject from "$lib/components/index/choose-project.svelte";
  import Hero from "$lib/components/index/hero.svelte";
  import SectionScreenshot from "$lib/components/index/section-ides.svelte";
  import Testimonials from "$lib/components/index/testimonials.svelte";
  import GetStarted from "$lib/components/index/get-started/index.svelte";
  import OpenGraph from "$lib/components/open-graph.svelte";
  import UsedBy from "$lib/components/index/used-by.svelte";
  import SpinUp from "$lib/components/index/spin-up.svelte";
  import Section from "$lib/components/section.svelte";
  import Resources from "$lib/components/resources.svelte";
</script>

<OpenGraph
  data={{
    description:
      "Gitpod streamlines developer workflows by providing prebuilt, collaborative developer environments in your browser - powered by VS Code.",
    title: "Gitpod - Always ready to code",
  }}
/>

<Hero />
<ChooseProject />
<div id="choose-project-observer-target-bottom">
  <Features {features} />
</div>
<SectionScreenshot />
<UsedBy
  title="Used by 500k+ developers"
  class="bg-off-white rounded-2xl shadow-normal pt-small pb-9"
/>
<Features features={otherFeatures} />
<Section>
  <Resources {cards} headingLevel="h2" />
</Section>
<Testimonials {testimonials} />
<GetStarted />
<SpinUp />
