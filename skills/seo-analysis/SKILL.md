---
name: seo-analysis
description: Analyze a site's organic search performance and identify the most impactful SEO fixes. Use when users ask for an SEO audit, traffic-drop diagnosis, keyword opportunities, metadata improvements, schema recommendations, or page-speed related search visibility issues.
allowed-tools: Read, Grep, Glob, Bash
---

# SEO Analysis

This skill helps Claude perform a practical SEO audit for a website, landing page, or content hub and turn the findings into prioritized actions.

## Overview

Use this skill to evaluate how well a page or site can perform in organic search. It focuses on the issues that most often affect rankings, click-through rate, and indexability:

1. Technical crawl and indexing blockers
2. Metadata quality and search snippet alignment
3. Content gaps and search intent mismatch
4. Internal linking and information architecture
5. Structured data opportunities
6. Page speed and Core Web Vitals risk areas

## Core Features

1. **Technical SEO Review**
   - Check crawlability, canonicalization, duplicate content risk, broken links, redirects, robots directives, and sitemap coverage.
2. **On-Page SEO Review**
   - Evaluate title tags, meta descriptions, heading structure, content depth, keyword targeting, and content freshness.
3. **Search Intent Analysis**
   - Compare the page's message to the likely intent behind target queries and identify mismatches.
4. **Schema & SERP Enhancement Review**
   - Recommend structured data improvements that can improve eligibility for richer results.
5. **Performance Review**
   - Flag page speed and UX issues that can hurt search performance or user engagement.
6. **Action Plan Generation**
   - Produce a short, prioritized plan with high-impact fixes first.

## When to Use This Skill

Activate this skill when a user asks things like:

- "Audit my site's SEO"
- "Why did our organic traffic drop?"
- "How can I improve rankings for this page?"
- "Check our title tags and metadata"
- "What schema should this page use?"
- "Find SEO issues on this landing page"

## Inputs

The skill works best with:

- A target URL or domain
- Optional target keywords
- Optional business context or audience
- Optional analytics or Search Console observations from the user

If the user does not provide all inputs, ask only for the missing items that materially change the audit.

## Workflow

### Step 1: Confirm Scope

Clarify whether the user wants:

- A single-page audit
- A section-level audit
- A full-site directional audit
- A traffic-drop investigation

### Step 2: Gather Context

Collect:

- Target URL
- Main conversion goal
- Primary audience
- Important keywords or topics
- Any known traffic or ranking problems

### Step 3: Run the Audit

Inspect the page or site for:

1. **Indexability**
   - `noindex`, canonicals, robots directives, redirect chains, crawl traps
2. **Metadata**
   - Title tag clarity, uniqueness, keyword alignment, meta description quality
3. **Content Quality**
   - Intent match, topical completeness, duplication, thin content, weak headings
4. **Internal Linking**
   - Orphan risks, weak anchor text, poor contextual linking
5. **Structured Data**
   - Missing or incorrect schema types, validation risks, rich-result opportunities
6. **Performance**
   - Slow templates, media bloat, render-blocking resources, mobile UX concerns

### Step 4: Prioritize Findings

Group recommendations by impact:

1. **Critical**
   - Indexing or crawl issues blocking discovery
2. **High**
   - Metadata, intent, or structural issues limiting rankings or CTR
3. **Medium**
   - Schema, linking, and content-depth improvements
4. **Low**
   - Polish items and secondary opportunities

### Step 5: Deliver Actionable Output

Return:

1. Top problems found
2. Why they matter
3. What to change
4. Expected upside
5. A 30-day priority plan

## Output Format

Use this structure for final answers:

### SEO Summary
- One-paragraph summary of the site's current SEO state

### Top Findings
1. Finding
2. Impact
3. Recommended fix

### Quick Wins
- 3 to 5 actions that can be implemented quickly

### Longer-Term Opportunities
- Higher-effort improvements with strategic payoff

### 30-Day Plan
- Week 1
- Week 2
- Week 3
- Week 4

## Example Usage

### Example 1

**User request:**  
"Audit the SEO for `https://example.com/pricing` and tell me what to fix first."

**Expected behavior:**  
Review the pricing page for metadata, heading structure, intent alignment, internal links, schema opportunities, and performance risks. Return a prioritized fix list with a concise action plan.

### Example 2

**User request:**  
"Our blog traffic dropped after the redesign. What should we check?"

**Expected behavior:**  
Investigate likely causes such as missing metadata, changed URL structure, broken canonicals, weak internal links, content pruning, page speed regressions, and indexability issues. Focus on the highest-probability explanations first.

## Tips

- Avoid generic SEO advice that does not map to the user's page or business goal.
- Prioritize issues that affect indexability, rankings, and click-through rate before cosmetic improvements.
- When data is incomplete, state assumptions clearly.
- Recommend the smallest set of changes most likely to move results.
