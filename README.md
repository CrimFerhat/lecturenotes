---
title: "Lecture notes - Week 1"
author: "Dr Ferhat Tura"
format: html
editor: visual
---

# **Session 1: Introduction**

## **What is Quantitative Social Science?**

Quantitative Social Science is the application of numerical data and statistical methods to understand and analyse social phenomena. It provides a systematic approach to studying human behaviour, social structures, and interactions by focusing on measurable evidence.

In this field, researchers use data to answer questions about society, such as:

-   What factors influence crime rates in urban areas?

-   How do socioeconomic conditions affect access to education?

-   What is the relationship between income inequality and social trust?

**Key Features of Quantitative Social Science:**

1.  **Data-Driven Insights**: Researchers collect and analyse data, often using surveys, experiments, or administrative records, to uncover patterns and relationships.

2.  **Statistical Rigour**: Methods such as regression analysis, hypothesis testing, and machine learning models are used to ensure conclusions are reliable and valid.

3.  **Generalisability**: Findings from quantitative research are often applicable to broader populations, making them essential for policymaking and evidence-based practices.

4.  **Comparative Analysis**: Quantitative approaches allow comparisons across different groups, regions, or time periods to identify trends and disparities.

## Why Quantitative Methods Matter?

-   They help to test theories and hypotheses in a structured way.

-   Quantitative data can uncover causal relationships and predict future outcomes.

-   Policymakers and organisations rely on quantitative research to design effective interventions and allocate resources efficiently.

For example, a criminologist might use quantitative data to explore how neighbourhood-level unemployment affects crime rates, while a sociologist might analyse survey data to study changes in public attitudes towards immigration over time.

In summary, Quantitative Social Science equips researchers with tools to address complex societal challenges, offering evidence-based solutions that can drive meaningful change.

# **Session 2: Introduction to R and RStudio**

## **Finding and Installing R and RStudio**

R and RStudio are essential tools for conducting data analysis in R. This section outlines how to find, download, and install these software packages.

**Step 1: Installing R**

R is the programming language at the core of our analysis. To install R:

1.  Visit the [Comprehensive R Archive Network (CRAN)](https://cran.r-project.org/).

2.  Select your operating system:

    -   **Windows**: Click on Download R for Windows and follow the prompts to download the installer.

    -   **macOS**: Click on Download R for macOS and select the appropriate version for your system.

    -   **Linux**: Choose the link for your Linux distribution and follow the provided instructions.

3.  Once downloaded, run the installer and follow the on-screen instructions to complete the setup.

**Step 2: Installing RStudio**

RStudio is an integrated development environment (IDE) designed to make working with R more efficient and user-friendly, offering advanced tools and an intuitive interface.

1.  Visit the [RStudio Desktop Download Page](https://posit.co/download/rstudio-desktop/).

2.  Download the free version (RStudio Desktop) that matches your operating system (Windows, Mac, or Linux).

3.  Run the installer and follow the on-screen instructions to complete the installation.

**Useful Links**

-   [R Documentation](https://cran.r-project.org/manuals.html) – Comprehensive guides and manuals for R.

-   [RStudio Documentation](https://posit.co/resources/) – Tutorials and resources to help you get started with RStudio.

-   [Introduction to R (via swirl)](https://swirlstats.com/students.html) – An interactive way to learn R directly within RStudio.

By completing these steps, you’ll have both R and RStudio installed and ready for your quantitative research projects. If you encounter any issues during the process, feel free to reach out for support!

## **Environment and Layout of RStudio**

RStudio provides a powerful integrated development environment (IDE) for working with R. Its layout is designed to facilitate efficient data analysis, coding, and visualisation. The RStudio interface is organised into four main panels, each serving a different purpose. Understanding the layout of RStudio will help you navigate the software effectively and maximise your productivity. Here’s an overview of the RStudio environment:

**1. Console (Bottom Left Panel)**

The **Console** is where you interact directly with R. You can type R commands here and see the immediate output. This panel is essential for performing analysis, running code, and debugging.

-   **How to use**: Type commands directly into the Console and press **`Enter`** to execute. The results or error messages will be displayed below.

**2. Source (Top Left Panel)**

The **Source** pane is where you write and edit R scripts, R Markdown files, and other code documents. This is the main area for writing and saving your work.

-   **How to use**: Open a new script by clicking *File \> New File \> R Script* or *R Markdown*. Code written here can be saved, modified, and re-executed.

-   **Features**:

    -   **Syntax highlighting**: Makes it easier to read and write code by highlighting keywords and functions.

    -   **Line numbers**: Helps you navigate your script quickly.

    -   **Run Code**: Highlight code and click *Run* to execute it in the Console, or use the shortcut **`Ctrl+Enter`** (Windows) or **`Cmd+Enter`** (Mac).

**3. Environment and History (Top Right Panel)**

This panel contains two tabs: **Environment** and **History**.

-   **Environment**: Displays all the objects (such as variables, functions, data frames) currently in your R session. You can click on these objects to inspect their contents.

    -   For example, if you create a vector **`v1 <- c(1, 2, 3)`**, it will appear in the Environment tab, showing the object name and its contents.

-   **History**: Shows a log of all previously executed commands. You can browse your command history and reuse or modify previous commands.

**4. Files, Plots, Packages, Help, and Viewer (Bottom Right Panel)**

This multi-purpose panel has several tabs, which are useful for different tasks:

-   **Files**: Displays the files and directories in your working directory. You can navigate through your files, open scripts, and manage directories.

-   **Plots**: Shows any visualisations or plots that are generated from your R code. For example, if you run a plot command like **`plot(1:10)`**, the resulting plot will appear here.

-   **Packages**: Allows you to view and manage R packages. You can install new packages, load/unload them, and check which packages are currently loaded in your session.

-   **Help**: Provides access to R documentation. If you want help on a function or package, simply type **`?function_name`** in the Console or search for it in the Help tab. For example, typing **`?mean`** will bring up the documentation for the **`mean()`** function.

-   **Viewer**: Displays interactive content like Shiny apps, web pages, or interactive plots (if supported). This tab is often used when working with web-based tools or visualisation libraries.

**5. Customising RStudio Layout**

You can rearrange and resize these panels to suit your preferences. To change the layout:

1.  Go to *Tools \> Global Options*.

2.  Under the *Pane Layout* section, you can choose how you want your panels to be arranged (e.g., switching the Environment panel to the bottom).

**Summary of Key Components:**

-   **Console**: Execute commands and see output.

-   **Source**: Write and edit code.

-   **Environment and History**: Track variables and previous commands.

-   **Files, Plots, Packages, Help, Viewer**: Manage files, view plots, and access documentation.

This layout is designed to streamline the process of coding, visualising, and analysing in R. By becoming familiar with these panels, you can work more efficiently and stay organised as you conduct your analyses.

## **Working Directories**

In R, the **working directory** is the folder where R looks for files to read and where it saves files. Setting the correct working directory is essential for ensuring that R can access the data files and save results in the right location.

-   To **check** your current working directory, use the **`getwd()`** function:

```{r}
getwd()
```

This will return the current directory path.

To **change** your working directory, use the `setwd()` function followed by the path to the desired folder:

```{r}
setwd("C:/Users/ftura/OneDrive - Bournemouth University/FERHAT WORK BU/Teaching/L5 Quantitative Research Skills Semester 2 2024-25 R/QSS with R")
```

It’s good practice to set your working directory at the start of each session to ensure R can find the files it needs for your project. You can also use the *Session* menu in RStudio to set the working directory.

# **Session 3: R Basics**

## **Arithmetic and Objects**

R is a powerful language for performing arithmetic operations and storing data in **objects**. An object in R is a variable that holds a value, such as a number, text, or more complex data like vectors or data frames. You can assign values to objects using the **`<-`** operator (or **`=`** in some cases), and then use these objects in calculations or further analysis.

-   **Arithmetic operations** in R are straightforward and include basic operations such as addition, subtraction, multiplication, and division:

```{r}
3 + 3   # Addition
3 - 3   # Subtraction
3 * 3   # Multiplication
3 / 3   # Division
```

-   **Creating objects** allows you to store results for later use. For example:

```{r}
a <- 3 + 3   # Assigns the result of 3 + 3 to object 'a'
a

b <- 3 * 3   # Assigns the result of 3 * 3 to object 'b'
b
```

## **Vectors, Matrices, and Data Frames**

**What Are They?**

-   **Vector**: A one-dimensional collection of data (e.g., numbers) in a specific order.

-   **Matrix**: A two-dimensional array of numbers with rows and columns.

-   **Data Frame**: A matrix treated as a dataset, similar to a spreadsheet. Columns are variables, rows are observations.

-   **Tibble**: A data frame in the **`tidyverse`** ecosystem with better formatting and printing.

Once assigned, these objects can be used in more complex operations, helping to organise and reuse data throughout your analysis.

**Creating Vectors**

In R, a **vector** is a basic data structure that holds an ordered collection of elements, typically of the same type (e.g., numeric, character, or logical). Vectors are essential for data manipulation and analysis in R.

You can create vectors using the **`c()`** function, which combines individual elements into a single vector.

**Example: Creating a Numeric Vector**

```{r}
# Create a vector
v1 <- c(1, 2, 3, 4, 5) # A vector of numbers from 1 to 5
v1

# Create another vector
v2 <- c(6, 7, 8, 9, 10)
v2

# Combine the vectors
v3 <- c(v1, v2)
v3

# Now,v3 is a variable with 10 observations.
```

**Example: Creating a Character Vector**

```{r}
v4 <- c("apple", "banana", "cherry")  # A vector of fruits
v4
```

**Example: Creating a Logical Vector**

```{r}
v5 <- c(TRUE, FALSE, TRUE)  # A vector of logical values (TRUE/FALSE)
v5
```

**Converting a Vector into a Data Frame**

```{r}
# Turn the vector v3 into a data frame
df1 <- as.data.frame(v3)
df1
```

# **Session 4: Installing and Loading Packages in R**

**Installing the `tidyverse` Package**

```{r}
# Install tidyverse package
install.packages("tidyverse")
```

**Loading the `tidyverse` Package**

```{r}
# Load/Activate tidyverse package
library(tidyverse)
```

**What’s Next?**

-   After loading the **`tidyverse`**, you can use its functions for data analysis.

-   Examples and more details will follow in future chapters.

# **Session 5: Finding Data**

## **Primary Data: Collecting Your Own Data**

Primary data refers to data that you collect yourself through surveys, experiments, interviews, or observations. This type of data is tailored to your specific research questions and allows for control over the data collection process, ensuring it meets your study’s needs.

## **Secondary Data: Data Collected by Others**

Secondary data is data that has already been collected and is available for use. This can include datasets from previous research, government statistics, or open-access data repositories. Using secondary data saves time and resources, but it’s important to evaluate its relevance and quality for your research.

## **Sources of Secondary Data**

**Library Resources**

University libraries often provide access to extensive collections of secondary data, including academic publications, journals, and specialised datasets. Librarians can guide you to appropriate resources for your research needs.

**Data Repositories**

Data repositories are online platforms that host a variety of datasets for public or restricted use. They are excellent sources for obtaining structured, high-quality data for analysis. Key repositories include:

-   **UK Data Service**: A comprehensive resource for social science and economic data, offering access to UK-specific datasets such as the British Social Attitudes Survey or the Labour Force Survey.\
    [Visit the UK Data Service](https://ukdataservice.ac.uk/)

-   **ICPSR (Inter-university Consortium for Political and Social Research)**: A leading repository for international social science research data.\
    Visit ICPSR

-   **Harvard Dataverse**: An open-access repository with datasets from various disciplines.\
    [Visit Harvard Dataverse](https://dataverse.harvard.edu/)

**Government Sources**

Government agencies publish a wealth of statistical data, often free of charge. Examples include:

-   The UK’s **Office for National Statistics (ONS)**: [Visit ONS](https://www.ons.gov.uk/)

-   Local government or public sector organisations, which may provide data relevant to specific regions or topics.

**Asking Someone**

Sometimes, the best data source can be an expert in your field. Reaching out to researchers, practitioners, or organisations may give you access to unique datasets not readily available online. Networking and collaboration can be valuable tools in locating the data you need.

By understanding the variety of data sources available, you can select the most suitable ones for your research while considering factors such as accessibility, quality, and relevance.

# **Session 6: Data Management**

## **The World of Tidyverse**

The **Tidyverse** is a collection of R packages designed to simplify and standardise data management, manipulation, and visualisation. These packages share a consistent syntax and philosophy, making it easier to work with data in R.

Key packages in the Tidyverse include:

-   **dplyr** for data manipulation.

-   **ggplot2** for data visualisation.

-   **readr** for reading various types of data files.

Additionally, the Tidyverse ecosystem extends beyond its core packages, incorporating others such as:

-   **haven** for reading SPSS, Stata, and SAS files.

-   **readxl** for reading Excel files.

-   **lubridate** for working with date and time data.

Throughout this chapter, we will explore how to use these tools effectively.

## **How to Read in Data**

Before working with data in R, it’s important to understand how to load data files from your working directory.

-   To check your working directory:

```{r}
getwd()
```

-   Make sure your directory contains a folder named **`Data`** where you store datasets for your analysis.

**Common File Formats**

Here are some of the most commonly used data file formats:

-   **Comma-separated values (.csv)**

-   **Text files (.txt)**

-   **Table files (.tab)**

-   **Excel files (.xlsx)**

-   Files from other statistical software:

    -   **Stata (.dta)**

    -   **SPSS (.sav)**

    -   **SAS (.sas7bdat)**

-   **R’s own format (.RData)**

**Reading Files in R**

**Reading `.csv` Files**

The **`read_csv()`** function from the **`readr`** package (part of Tidyverse) is used for reading CSV files as tibbles:

```{r}
csvdata <- read_csv("Data/2020 Scottish Index of Multiple Deprivation/simd2020.csv", na = "*")
```

**Reading Excel Files**

To read Excel files, use the **`readxl`** package:

```{r}
library(readxl)

# For older Excel files
# xlsxdata <- read_xls("Data/example_file.xls")

# For newer Excel files
# xlsxdata <- read_xlsx("Data/example_file.xlsx")

# If the Excel version is unknown
# xlsxdata <- read_excel("Data/example_file.xlsx")
```

**Reading `.txt` and `.tab` Files**

Use **`read_delim()`** from **`readr`** for text or tab-delimited files:

```{r}
# txtdata <- read_delim("Data/example_file.txt", delim = "\t", na = "*")
# tabdata <- read_delim("Data/example_file.tab", delim = "\t", na = "*")
```

**Reading Stata Files**

Use the **`haven`** package to read Stata files:

```{r}
library(haven)
# dtadata <- read_dta("Data/example_file.dta")
```

**Reading SPSS Files**

Use the **`haven`** package to read SPSS files:

```{r}
# savdata <- read_sav("Data/example_file.sav")
```

**Reading SAS Files**

Use the **`haven`** package to read SAS files:

```{r}
# sasdata <- read_sas("Data/example_file.sas7bdat")
```

**Using RStudio's Import Dataset Option**

For a graphical interface, use RStudio's **Import Dataset** feature available in the Environment pane. This tool simplifies importing data without writing code and provides a preview of the dataset before loading it into R.

By mastering these techniques, you’ll be able to load a variety of datasets into R, enabling you to begin your data analysis efficiently.

# **Summary**

-   **Quantitative Social Science**:

    -   Focuses on using numerical data and statistical methods to understand social phenomena.

    -   Key features include data-driven insights, statistical rigour, generalisability, and comparative analysis.

-   **Installing R and RStudio**:

    -   R is the core programming language for data analysis.

    -   RStudio is a user-friendly IDE for working with R.

-   **RStudio Environment**:

    -   Four panels: Console, Source, Environment & History, and Files/Plots/Packages/Help.

    -   Customisable layout for streamlined workflows.

-   **R Basics**:

    -   Arithmetic operations and creating objects (**`<-`**) to store values.

    -   Understanding vectors, matrices, data frames, and tibbles as key data structures.

-   **Finding Data**:

    -   Primary data: Collected through surveys, experiments, or observations.

    -   Secondary data: Available from libraries, government sources, or repositories like the UK Data Service, ICPSR, and Harvard Dataverse.

-   **Data Management with Tidyverse**:

    -   Introduction to **`tidyverse`** packages for data manipulation (**`dplyr`**), visualisation (**`ggplot2`**), and importing files (**`readr`**).

    -   Handling common file formats like **`.csv`**, **`.xlsx`**, **`.dta`**, and **`.sav`**.

    -   Using **`read_*`** functions or RStudio's Import Dataset tool for loading data.

**Takeaway:**

This week established foundational skills for understanding Quantitative Social Science and working with R and RStudio. These are essential for effective data analysis, setting the stage for more advanced topics in future sessions.

