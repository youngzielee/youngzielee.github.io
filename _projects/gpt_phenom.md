---
layout: distill
title: sentence qualia structure
description: Modeling phenomenal similarity of global states of consciousness leveraging LLMs
img: assets/img/gpt_thumbnail.png
importance: 1
category: work
related_publications: true
tags: qualia
giscus_comments: false
date: 2024-05-17
featured: true

authors:
  - name: Zoe Youngzie Lee
    affiliations:
      name: UCLA
  - name: Norie Kawamura
    affiliations:
      name: ATR   
  - name: Naotsugu Tsuchiya
    affiliations:
      name: Monash University
  - name: Martin Monti
    affiliations:
      name: UCLA


# bibliography: 2018-12-22-distill.bib

# Optionally, you can add a table of contents to your post.
# NOTES:
#   - make sure that TOC names match the actual section names
#     for hyperlinks within the post to work correctly.
#   - we may want to automate TOC generation in the future using
#     jekyll-toc plugin (https://github.com/toshimaru/jekyll-toc).
toc:
  - name: Background
    # if a section has subsections, you can add them as follows:
    # subsections:
    #   - name: Example Child Subsection 1
    #   - name: Example Child Subsection 2
  - name: Methods
  - name: Interactive Plots


# Below is an example of injecting additional post-specific styles.
# If you use this post as a template, delete this _styles block.
_styles: >
  .fake-img {
    background: #bbb;
    border: 1px solid rgba(0, 0, 0, 0.1);
    box-shadow: 0 0px 4px rgba(0, 0, 0, 0.1);
    margin-bottom: 12px;
  }
  .fake-img p {
    font-family: monospace;
    color: white;
    text-align: left;
    margin: 12px 0;
    text-align: center;
    font-size: 16px;
  }
---

## (Very brief) Introduction

We leveraged LLMs to derive the similarity structure between phenomenal experiences described in short sentences.
Our data--sentences borrowed from existing phenomenology questionnaires--can be viewed [here](https://docs.google.com/spreadsheets/d/1Qjf4khRy6IRu-43Q1t3ntakoJ3E2LWPdI5j8iIMIAb8/edit?usp=sharing).


---

## Methods

We prompted GPT4 (gpt-4-0125-preview) to generate answers "describing an internal aspect of what that experience feels like, such as sensations, perceptions, emotions, or thoughts." Then, we used nonnegative matrix factorization to extract 50 latent dimensions of phenomenal features. These dimensions seemed to be hierarchical, and we merged some topics (4, 43, 36, 27, 8, 24, 20, 0), resulting in the final 46 topics.

{% details Click here for hierarchical structure of topics %}
````markdown
.
├─curiosity_sudden_curious_surprise_pique ── Topic: 88
│    ├─curiosity_curious_pique_curiosity pique_intrigue ── Topic: 77
│    │    ├─O curiosity_pique_curiosity pique_spark_curiosity spark ── Topic: 4
│    │    └─O curious_intrigue_unknown_openness_surprised ── Topic: 43
│    └─sudden_surprise_sudden clarity_surge_momentary ── Topic: 63
│         ├─O surprise_sudden_momentary_fleet_unexpected ── Topic: 36
│         └─O sudden_sudden clarity_surge_rush_adrenaline ── Topic: 27
└─focus_heighten_attention_focused_heighten focus ── Topic: 97
     ├─heighten_emotion_awareness_overwhelm_profound ── Topic: 96
     │    ├─heighten_emotion_awareness_awareness heighten_heighten awareness ── Topic: 94
     │    │    ├─heighten_emotion_awareness_awareness heighten_heighten awareness ── Topic: 70
     │    │    │    ├─O heighten_awareness_awareness heighten_heighten awareness_alertness ── Topic: 7
     │    │    │    └─O emotion_intensify_flow_heighten_thought ── Topic: 33
     │    │    └─anticipation_sensation_thought_inside_float ── Topic: 93
     │    │         ├─anticipation_thought_anxious_mind_anxiety ── Topic: 89
     │    │         │    ├─thought_mind_anxious_heart_overwhelm ── Topic: 82
     │    │         │    │    ├─heart_overwhelm_race_stomach_thought ── Topic: 78
     │    │         │    │    │    ├─desire_restless_overwhelm_scatter_distract ── Topic: 73
     │    │         │    │    │    │    ├─O desire_discomfort_escape_longing_nausea ── Topic: 45
     │    │         │    │    │    │    └─O restless_scatter_distract_easily_thought scatter ── Topic: 39
     │    │         │    │    │    └─heart_race_overwhelm_stomach_well ── Topic: 69
     │    │         │    │    │         ├─race_heart_thought_stomach_heart race ── Topic: 53
     │    │         │    │    │         │    ├─O race_heart_heart race_race thought_thought ── Topic: 1
     │    │         │    │    │         │    └─O stomach_thought_chest_knot_stomach knot ── Topic: 12
     │    │         │    │    │         └─O overwhelm_well_heavy_tear_sadness ── Topic: 25
     │    │         │    │    └─thought_mind_anxious_within_overwhelmed ── Topic: 80
     │    │         │    │         ├─thought_anxious_within_overwhelmed_swirl ── Topic: 62
     │    │         │    │         │    ├─O anxious_overwhelmed_thought_swirl_rise ── Topic: 11
     │    │         │    │         │    └─thought_within_clarity thought_cloud_stir ── Topic: 59
     │    │         │    │         │         ├─O thought_clarity thought_overwhelm thought_moment_absorb ── Topic: 3
     │    │         │    │         │         └─O within_thought_cloud_stir_cloud thought ── Topic: 30
     │    │         │    │         └─mind_thought_foggy_contentment_ease ── Topic: 55
     │    │         │    │              ├─O mind_foggy_thought_wander_heavy ── Topic: 10
     │    │         │    │              └─O contentment_ease_mind_envelop_thought ── Topic: 38
     │    │         │    └─anticipation_anxiety_anxious anticipation_frustration_grow ── Topic: 83
     │    │         │         ├─O anticipation_anxious anticipation_anxious_excitement_eager ── Topic: 18
     │    │         │         └─frustration_grow_control_anxiety_loss ── Topic: 81
     │    │         │              ├─frustration_grow_frustrate_impatience_mount ── Topic: 57
     │    │         │              │    ├─O frustration_frustrate_mount_grow_frustration grow ── Topic: 31
     │    │         │              │    └─O grow_impatience_impatience grow_drag_restlessness ── Topic: 21
     │    │         │              └─control_anxiety_loss_fear_loss control ── Topic: 72
     │    │         │                   ├─O anxiety_fear_judgment_spike_self-doubt ── Topic: 34
     │    │         │                   └─O control_loss_loss control_lose_helplessness ── Topic: 16
     │    │         └─sensation_float_tingle_inside_emptiness ── Topic: 91
     │    │              ├─inside_emptiness_time_lose_confusion ── Topic: 87
     │    │              │    ├─inside_emptiness_detach_emotional_emotionally ── Topic: 74
     │    │              │    │    ├─O inside_emptiness_emptiness inside_fade_empty ── Topic: 41
     │    │              │    │    └─detach_emotional_emotionally_detachment_disconnect ── Topic: 54
     │    │              │    │         ├─O emotional_detachment_emotional detachment_numbness_detach ── Topic: 8
     │    │              │    │         └─O emotionally_detach_surroundings_disconnect_emotionally detach ── Topic: 24
     │    │              │    └─time_confusion_lose_confuse_disorient ── Topic: 86
     │    │              │         ├─O time_lose_lose time_intense_intense focus ── Topic: 26
     │    │              │         └─confusion_confuse_disorient_slight_sensation ── Topic: 64
     │    │              │              ├─confuse_disorient_lose_perception_confusion ── Topic: 56
     │    │              │              │    ├─O confuse_lose_confusion_disorient_thought lose ── Topic: 15
     │    │              │              │    └─O disorient_perception_reality_surreal_disorientation ── Topic: 49
     │    │              │              └─O confusion_slight_sensation_slight confusion_mild ── Topic: 37
     │    │              └─sensation_float_tingle_heartbeat_quicken ── Topic: 68
     │    │                   ├─O sensation_float_freedom_weightless_peaceful ── Topic: 14
     │    │                   └─O tingle_heartbeat_sensation_quicken_skin ── Topic: 22
     │    └─overwhelm_profound_joy_warmth_clarity ── Topic: 95
     │         ├─overwhelm_profound_joy_bubble_boundless ── Topic: 75
     │         │    ├─profound_overwhelm_peace_awe_boundless ── Topic: 50
     │         │    │    ├─O profound_peace_boundless_unity_timelessness ── Topic: 32
     │         │    │    └─O overwhelm_profound_awe_gratitude_profound awe ── Topic: 6
     │         │    └─joy_bubble_overwhelm joy_overwhelm_heart ── Topic: 51
     │         │         ├─O joy_overwhelm joy_overwhelm_heart_swell ── Topic: 13
     │         │         └─O bubble_joy_eye_inside_joy bubble ── Topic: 44
     │         └─warmth_clarity_emotional_inner_mental ── Topic: 92
     │              ├─warmth_emotional_spread_nostalgia_warmth spread ── Topic: 85
     │              │    ├─emotional_vivid_connection_color_deeply ── Topic: 79
     │              │    │    ├─vivid_color_emotional_imagery_vivid imagery ── Topic: 52
     │              │    │    │    ├─O color_shift_vivid color_intrigue_eye ── Topic: 28
     │              │    │    │    └─O vivid_emotional_imagery_vivid imagery_image ── Topic: 23
     │              │    │    └─emotional_connection_deeply_deep_introspective ── Topic: 67
     │              │    │         ├─emotional_connection_deep_intense_relief ── Topic: 65
     │              │    │         │    ├─O emotional_intense_relief_understanding_intensity ── Topic: 48
     │              │    │         │    └─O connection_deep_emotional_empathy_deep connection ── Topic: 29
     │              │    │         └─O deeply_introspective_self-awareness_emotional_introspection ── Topic: 42
     │              │    └─warmth_spread_nostalgia_warmth spread_emotional ── Topic: 61
     │              │         ├─O nostalgia_warmth_emotional_wash_nostalgic ── Topic: 5
     │              │         └─O warmth_spread_warmth spread_inside_chest ── Topic: 2
     │              └─clarity_inner_mental_calmness_peace ── Topic: 90
     │                   ├─inner_calmness_peace_empower_inner peace ── Topic: 84
     │                   │    ├─empower_inner_confident_energize_confidence ── Topic: 58
     │                   │    │    ├─O energize_idea_hopeful_creativity_motivate ── Topic: 46
     │                   │    │    └─O empower_inner_confident_confidence_strength ── Topic: 35
     │                   │    └─inner_calmness_peace_inner peace_tension ── Topic: 71
     │                   │         ├─inner_calmness_peace_inner peace_deep ── Topic: 60
     │                   │         │    ├─O calmness_inner_calm_peaceful_stillness ── Topic: 20
     │                   │         │    └─O inner_peace_inner peace_deep_deep inner ── Topic: 0
     │                   │         └─O inner_tension_moment_turmoil_conflict ── Topic: 40
     │                   └─clarity_mental_inner_dialogue_fog ── Topic: 76
     │                        ├─O inner_dialogue_echo_inner dialogue_voice ── Topic: 47
     │                        └─clarity_mental_fog_mental fog_exhaustion ── Topic: 66
     │                             ├─O mental_fog_mental fog_exhaustion_mental exhaustion ── Topic: 17
     │                             └─O clarity_mental_mental clarity_emerge_emotional ── Topic: 9
     └─O focus_attention_focused_heighten focus_mind ── Topic: 19

````
{% enddetails %}


Comparison of similarity structure after topic modeling and merging
<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/similarity_heatmaps_comparison_postmerge_gpt4-turbo-preview_041624.html' | relative_url }}" frameborder='0' scrolling='yes' height="500px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>


---

## Interactive Plots

These are the phenomenological topics we get (pretty coherent and interpretable!):

<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/46topics_pyldavis_gpt4-turbo-preview_041624.html' | relative_url }}" frameborder='0' scrolling='yes' height="1000px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>

which create coherent clusters of items based on phenomenological similarity, not semantic similarity:

<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/affinity_clusters_tsne_043024.html' | relative_url }}" frameborder='0' scrolling='yes' height="600px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>

Similarity structure of cluster centroids (exemplars):
<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/affinity_exemplars_similarity_heatmap_043024.html' | relative_url }}" frameborder='0' scrolling='yes' height="600px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>


We compared this model-derived similarity structure of 70 items with human-judgment-based similarity structures:
<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/similarity_matrices_70 items_46topics.html' | relative_url }}" frameborder='0' scrolling='yes' height="600px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>

Correlation between model v. humans (feature-agreement): r=0.35 (lower-bound: r=0.26), p<0.001
Correlation between model v. humans (pairwise-judgment): r=0.23, p<0.001
Correlation between humans (feature-agreement) v. humans (pairwise-judgment): r=0.22, p<0.001



Since our data comes from phenomenology questionnaires, we can see 'where in the space' each questionnaire item covers (in the legend, double-click on 'trace 0' and single-click on the instrument of interest):
<div class="l-page">
  <iframe src="{{ '/assets/plotly/gpt_phenomenology_plots/affinity_clusters_tsne_instrument_groups_070424.html' | relative_url }}" frameborder='0' scrolling='yes' height="600px" width="100%" style="border: 1px dashed grey;"></iframe>
</div>
