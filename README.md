Introduction
-----------

This is a git clone of https://jflex.svn.sourceforge.net/svnroot/jflex/trunk/maven-jflex-plugin/.

I modified it to support JetBrains's patched JFlex. See http://confluence.jetbrains.net/display/IDEADEV/Developing+Custom+Language+Plugins+for+IntelliJ+IDEA for more details.

All credit goes to original authors of JFlex, the maven plugin, and JetBrains.

Usage
-----

The meaningful modifications to this plugin are on the idea branch. Make sure to check it out before proceeding.

This plugin is dependent on IntelliJ's JFlex.jar. You can grab it by:

    git clone git://github.com/JetBrains/intellij-community.git
    cd intellij-community
    git checkout idea/117.798
    cd tools/lexer/jflex-1.4/lib
    mvn install:install-file -Dfile=JFlex.jar -DgroupId=de.jflex -DartifactId=jflex -Dversion=1.4.3.idea.11.1.3 -Dpackaging=jar

You can then install the plugin locally by doing:

    mvn install
