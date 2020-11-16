# Priscilla's Resume Template  
<img src="https://img.shields.io/badge/latex%20-%23008080.svg?&style=for-the-badge&logo=latex&logoColor=white"/>

This repo houses the LaTex template used to generate my resume.  
The template I used is forked from [here](https://github.com/darwiin/yaac-another-awesome-cv). 


## Relevant Files Used

```
--example
	|---- cv.tex					| Personal Information and links; Include/ Exclude sections in/from resume
	|---- section_competences.tex			| Used as skills section of my resume
	|---- section_experience_short.tex		| List of all work experiences and corresponding skill tags
	|---- section_projets.tex			| Project section
	|---- section_scolarite.tex			| Education section  
```


## Some Useful Info for Modifying Sections

### Set the left column size

Sections share the left column size (2.5cm by default). You can change this default size using the `\setleftcolumnlength` command.

```latex
% Override default left column length of (2.5cm) (optional)
% Usage: \setleftcolumnlength{1.5cm} to change the left column lengtyh to 1.5cm
% I recommend to use a size between 1.5cm to 2.5cm
\setleftcolumnlength{1.5cm}
``


### Construct the _comptences_ or _skills_ section

To list your awesome skills as keyword lists you first have to declare the `keywords` environment and then fill it with a list of keywordsentry

```latex
% Begin a new keywords environment to show us your awesome keywords
  \begin{keywords}
    
    % Here's go your keyword lists group by categories
    \keywordsentry{Frameworks}{Spring, Spring Boot, \textbf{Ionic 3}, Angular 2, Angular 4, ZK, JBoss RichFaces}
  \end{keywords}
```

### Construct the _experiences_ section

To describe your experiences you have first to declare the `experiences` environment

```latex
% Begin a new experiences environment to use experience and consultantexperience macro
\begin{experiences}

% Here's go your experiences

\end{experiences}
```

Then you can describe your experiences using **\experience** and **\consultantexperience** entries. Each
entry must be separated by the **\emptyseparator** 

```latex
% Begin a new experiences environment to use experience and consultantexperience macro
\begin{experiences}

% The experience entry work as below and can be used to describe a job experience
  \experience
    {End date}      {Experience title}{Enterprise}{Country}
    {Begin date}    {
    				  experience details
                      \begin{itemize}
                        \item Item 1: _Item 1 description_
                        \item Item 2: _Item 2 description_
                        \item Item 3: _Item 3 description_
                      \end{itemize}
                    }
                    {Technology highlights}

% The emptyseparator macro is used to create white space in your experience
  \emptySeparator

% The consultantexperience macro is very similar to the experience macro, but offer you 
% the possibility tu put client details
  \consultantexperience
    {End date}        {Experience title}{Enterprise}{Country}
    {Begin date}      {Client job title}{Clent enterprise}
                    {
                      experience details
                      \begin{itemize}
                        \item Item 1: _Item 1 description_
                        \item Item 2: _Item 2 description_
                        \item Item 3: _Item 3 description_
                      \end{itemize}
                    }
                    {Technology highlights}
\end{experiences}
```

### Construct the _languages_ section

The _languages_ section use the **skills** environment. 

```latex
% Begin a new skills environment and fill it with skill entries
  \begin{skills}

% Render a skill in the skills environment
% Usage: \skill{<skill>}{<level between 1 and 5>}
    \skill{Français}{5}
    \skill{Anglais}{4}

% End the skills environment    
  \end{skills}
```

### Construct the _scolarship_ section

The _scolarship_ section use the **scolarship** environment.

```latex
\begin{scholarship}

  % Render a scholarshipentry in the scolarship environment
  % Usage: \scholarshipentry{<date>}{<description>}
  \scholarshipentry{2007}
    {Master STIC Professionel filière MBDS de l'Université de Nice Sophia Antipolis (Master Informatique spécialité Multimédia, Base de Données et intégration de Systèmes)}
  \scholarshipentry{2005}
    {Licence Sciences et Technologies, Mention Informatique, de l'Université de Nouvelle-Calédonie}
\end{scholarship}
```

### Construct the _projects_ section

The _projects_ section use the **projects** environment.

```latex
\begin{projects}
  \project
    {Simply City}{2017 - 2018}
    {\website{https://www.simplycity.nc}{https://www.simplycity.nc} \website{https://innovation.engie.com/fr/news/actus/territoires/simply-city-lappli-qui-simplifie-la-ville-au-ces-2018-avec-engie/8156}{Présentation CES 2018} }
    {Simply City est une application mobile, gratuite et participative destinée à tous les habitants, visiteurs et touristes qui séjournent dans une ville. L’application permet de connaître toutes les informations et services utiles en temps réel.}
    {Ionic 3,Typescript,Javascript,Visual Studio Code}
        
\end{projects}
```

### Construct the _references_ section

The _references_ section use the **references** environment.

```latex
  \begin{references}

    % Here's go your references

  \end{references}
```

Then you can list your references as follow:

```latex
  \begin{referees}
    \referee
      {John Snow}
      {Lord Commander of the Night Watch}
      {Night Watch}
      {john.snow@nightwatch.org}
      {+687 987 654}

    \referee
      {Géry Loutre}
      {Architecte logiciel}
      {Cafat}
      {ref1@cafat.nc}
      {+687 987 654}

  \begin{referees}
```

