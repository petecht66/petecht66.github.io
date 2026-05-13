---
layout: post
title: Defensive Pass Coverage Variability and Its Success in the Modern NFL
subtitle: Does High Variability in Coverage Scheme Usage Lead to Successful Pass Defense?
thumbnail-img: /assets/img/NFLlogo.png
gh-repo: petecht66/defensive-pass-coverage-variability-success-NFL
gh-badge: [star, fork, follow]
tags: [R, Tableau, statistics, NFL]
comments: true
mathjax: true
author: Peter Chapman
---
<br><br>
# Project Overview
When discussing defensive strategy in the NFL, a common opinion among fans and the media is that mixing up defensive looks leads to successful defensive outcomes. For example, Kansas City Chiefs DC Steve Spagnuolo is known for his varied and disguised looks that confuse opposing offenses. However, high variation in defensive strategy does not guarantee success. In 2025, the Dallas Cowboys played a large majority of zone coverage through the first nine weeks of the regular season. Notably, the Cowboys' pass defense ranked near the bottom of the league during this stretch of the season.

This project focuses on the variation of defensive pass coverage schemes in the NFL during the first nine weeks of the NFL season. The goal of this study is to determine whether or not a high variation in defensive pass coverage scheme usage is correlated with a successful pass defense. The full [repository](https://github.com/petecht66/defensive-pass-coverage-variability-success-NFL) contains data collection and transformation in Excel, R programming scripts, data visualizations in Tableau, a complete report in .pdf and .docx forms, and a PowerPoint presentation.

## Standardized Entropy
A metric called **standardized entropy** was used to measure the variation in defensive pass coverage schemes for each NFL team in 2025. This statistics metric essentially takes the 

Ten PFF defensive pass coverage schemes were considered in the calcuation: Cover 0, Cover 1, Cover 1 Double, Cover 2, Cover 3, Quarter, Cover 6, Cover 2 Man, Cover 3 Seam, and Bracket Cover. These defensive pass coverage schemes are described in the full report. 

$$
\text{Coverage Standardized Entropy}_{\text{Team, Year}}
=
\frac{
\left|
\text{Cover 0 \%} \cdot \ln(\text{Cover 0 \%})
+
\text{Cover 1 \%} \cdot \ln(\text{Cover 1 \%})
+
\cdots
+
\text{Bracket Cover \%} \cdot \ln(\text{Bracket Cover \%})
\right|
}
{
\ln(\text{Number of Schemes} = 10)
}
.
$$