class: center, middle, inverse

# GitFlow Workshop

### by Thomas [@dikalikatao](http://twitter.com/dikalikatao)

---

class: center, middle, inverse

# GitFlow

## Mais qu'est ce que c'est ?


???

---
class: center

# C'est un cadre

![Cadre](cadre.png)


???

---
class: center

# Workflow

![git-workflow](git-workflow.png)

---
class: center

# Installation


```linux
Linux : apt-get install git-flow 

Mac : brew install git-flow OU port install git-flow
```

![soeasy](soeasy.jpg)

???

Bon, pour windows c'est quand même plus compliqué, voici la procédure :
https://github.com/nvie/gitflow/wiki/Windows#github-for-windows

---
class: center

# Commandes

![GitflowCommands](gitflow-commands.png)


---

# Exemples

```bash
	git flow feature start myNewFeature
 
	*[ ... On code la fonctionnalité
	et on écrit les tests qui vont biens ... ]*

	git commit -am "My new awesome feature !!!!111"

	git flow feature finish myNewFeature
```

---
class: center, middle, inverse

![demotime](demo.jpg)

---

class: middle

<div class="michu">
<img src="michu.png" width="180" height="220" class="author" />
<blockquote>"Ouai c'est bien beau tout ça mais si je veux utiliser facilement GitFlow dans mon projet Maven ?"<br/>
<span style="font-weight: bolder; font-size: 22px;">- Madame Michu, experte maven depuis 1832</span></blockquote>
</div>

# 

---

class: center, middle, inverse


# jgitflow

---

## Ajouter jgitflow à son projet

### Exemple de config :
```xml
<build>
    <plugins>
        <plugin>
            <groupId>external.atlassian.jgitflow</groupId>
            <artifactId>jgitflow-maven-plugin</artifactId>
            <version>1.0-m4.3</version>
            <configuration>
                    <flowInitContext>
                        <masterBranchName>master</masterBranchName>
                        <developBranchName>develop</developBranchName>
                        <featureBranchPrefix>feature-</featureBranchPrefix>
                        <releaseBranchPrefix>release-</releaseBranchPrefix>
                        <hotfixBranchPrefix>hotfix-</hotfixBranchPrefix>
                        <versionTagPrefix>protocat-</versionTagPrefix>
                    </flowInitContext>
                </configuration>
        </plugin>
    </plugins>
</build>
```
---
class: center, middle, inverse

## jgitflow : commandes

```shell
mvn jgitflow:feature-start
mvn jgitflow:feature-finish
mvn jgitflow:release-start
mvn jgitflow:release-finish
mvn jgitflow:hotfix-start
mvn jgitflow:hotfix-finish
mvn jgitflow:build-number 
```
---
class: center, middle

## 
<div class="michu">
<img src="robin.jpg" width="180" height="260" class="author" />
<blockquote>"Moi j'utilise SVN et je voudrais faire pareil !<br/>C'est possible ??"</blockquote>
</div>

???

---
class: center, middle, inverse

![svn](svn.jpg)

???

---
class: center, middle, inverse

![questions](questions.jpg)

