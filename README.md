# 🧪 Chemical Engineering Innovations for Luxury Leather Automobile Seats

![R](https://img.shields.io/badge/-R-276DC3?logo=r)
![ggplot2](https://img.shields.io/badge/-ggplot2-1f77b4)
![plotly](https://img.shields.io/badge/-plotly-d62728)
![dplyr](https://img.shields.io/badge/-dplyr-17becf)
![tidyr](https://img.shields.io/badge/-tidyr-e377c2)
![shiny](https://img.shields.io/badge/-shiny-17becf)
![bs4Dash](https://img.shields.io/badge/-bs4Dash-purple)
![shinyWidgets](https://img.shields.io/badge/-shinyWidgets-green)
![AspenPlus](https://img.shields.io/badge/-Aspen%20Plus-lightgrey)
![MATLAB](https://img.shields.io/badge/-MATLAB-orange)
![LabVIEW](https://img.shields.io/badge/-LabVIEW-yellow)
![Python](https://img.shields.io/badge/-Python-blue)

This repository contains a modernized case study and R-based visualizations exploring chemical engineering solutions for luxury leather seats in high-end vehicles. Prepared by **Maurice McDonald**, Data Viz Storyteller & US Army Veteran, for **Aeristo**, this report showcases sustainable innovations through an interactive Shiny dashboard and copy-ready R code blocks.

## 📁 Table of Contents

* [Introduction](#introduction)
* [Industry Context](#industry-context)
* [Chemical Engineering Projects](#chemical-engineering-projects)

  * [Eco-Friendly Tanning with Bio-Based Agents](#eco-friendly-tanning-with-bio-based-agents)
  * [Smart Leather with Embedded Sensors](#smart-leather-with-embedded-sensors)
  * [Nano-Coatings for Enhanced Durability](#nano-coatings-for-enhanced-durability)
* [Tech Stack](#tech-stack)
* [Implementation Strategy](#implementation-strategy)
* [Why These Projects Stand Out](#why-these-projects-stand-out)
* [R Shiny App: Optimization Dashboard](#r-shiny-app-leather-process-optimization-dashboard)
* [Repository Usage](#repository-usage)
* [Conclusion](#conclusion)
* [References](#references)
* [Author](#author)

---

## 📊 Introduction

Luxury leather interiors require sustainability, resilience, and smart materials. This report outlines 3 real-world chemical engineering innovations with embedded interactive and static R visualizations:

---

## ♻️ Eco-Friendly Tanning with Bio-Based Agents

```r
# R Graph Code
library(ggplot2)
library(dplyr)
set.seed(42)
tanning_data <- data.frame(
  Method = rep(c("Chromium", "Bio-Based"), each = 10),
  Time_Hours = c(runif(10, 8, 12), runif(10, 6, 10)),
  Water_Usage_Liters = c(runif(10, 500, 700), runif(10, 200, 400)),
  Quality_Score = c(runif(10, 0.8, 0.95), runif(10, 0.85, 0.98))
) %>% drop_na()
summary <- tanning_data %>% group_by(Method) %>% summarise(across(everything(), mean))

p <- ggplot(tanning_data, aes(x = Method, y = Water_Usage_Liters, fill = Method)) +
  geom_boxplot(width = 0.6, outlier.shape = NA) +
  scale_fill_manual(values = c("Chromium" = "#FF4500", "Bio-Based" = "#FFA500")) +
  theme_minimal() +
  theme(
    plot.background = element_rect(fill = "#000000"),
    panel.grid.major = element_line(color = "white", linetype = "dotted"),
    axis.text = element_text(color = "white"),
    axis.title = element_text(color = "white"),
    legend.text = element_text(color = "white"),
    legend.title = element_text(color = "white")) +
  labs(title = "Water Usage in Tanning", x = "Method", y = "Liters")
print(p)
```

---

## 🔥 Smart Leather with Embedded Sensors

```r
# R Graph Code
library(plotly)
sensor_data <- data.frame(
  Time_Min = seq(0, 60, by = 5),
  Temp_Traditional = 25 + 10 * sin(seq(0, pi, length.out = 13)),
  Temp_Smart = 25 + 2 * sin(seq(0, pi, length.out = 13))
)

plot_ly(sensor_data, x = ~Time_Min) %>%
  add_lines(y = ~Temp_Traditional, name = "Traditional Leather", line = list(color = "#FF4500")) %>%
  add_lines(y = ~Temp_Smart, name = "Smart Leather", line = list(color = "#1E90FF")) %>%
  layout(
    title = "Temperature Regulation in Leather Seats",
    xaxis = list(title = "Time (Minutes)"),
    yaxis = list(title = "Temperature (°C)"),
    paper_bgcolor = "#1A1A1A",
    plot_bgcolor = "#1A1A1A",
    font = list(color = "#D3D3D3"))
```

---

## 🛡️ Nano-Coatings for Enhanced Durability

```r
# R Graph Code
library(plotly)
abrasion_data <- data.frame(
  Cycles = seq(1000, 8000, by = 500),
  Wear_Uncoated = 0.5 - 0.00005 * seq(1000, 8000, by = 500),
  Wear_NanoCoated = 0.15 - 0.00001 * seq(1000, 8000, by = 500)
)

plot_ly(abrasion_data, x = ~Cycles) %>%
  add_lines(y = ~Wear_Uncoated, name = "Uncoated Leather", line = list(color = "#FF6347")) %>%
  add_lines(y = ~Wear_NanoCoated, name = "Nano-Coated Leather", line = list(color = "#4682B4")) %>%
  layout(
    title = "Abrasion Resistance of Leather Coatings",
    xaxis = list(title = "Abrasion Cycles"),
    yaxis = list(title = "Wear Score"),
    paper_bgcolor = "#1A1A1A",
    plot_bgcolor = "#1A1A1A",
    font = list(color = "#D3D3D3"))
```

---

## 🧠 R Shiny App: Leather Process Optimization Dashboard

```r
# Full Shiny App (app.R)
library(shiny)
library(bs4Dash)
library(plotly)
library(ggplot2)
library(dplyr)
library(tidyr)

ui <- bs4DashPage(...)
server <- function(input, output) { ... }
shinyApp(ui, server)
```

---

## 📦 Repository Usage

Clone repo → copy code → run in RStudio. Install:

```r
install.packages(c("shiny", "bs4Dash", "plotly", "ggplot2", "dplyr", "tidyr"))
```

---

## 👤 Author

Maurice McDonald
📊 Data Viz Storyteller | 🇺🇸 US Army Veteran
🔗 [LinkedIn](https://www.linkedin.com/in/mauricemcdonald) | [GitHub](https://github.com/emcdo411)
📅 June 18, 2025


