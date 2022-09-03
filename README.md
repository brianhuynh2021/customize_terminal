# Customize your own terminal
Color chart: https://upload.wikimedia.org/wikipedia/commons/1/15/Xterm_256color_chart.svg
Follow these steps and paste the code in your .bashrc file you can change your boring/static terminal into a dynamic terminal.

#Step 1: change the zsh commandline into bash by.
    
    chsh -s /bin/bash

#Step 2: open (or create) .bash_profile file and type command below and save it.<br>
    
    export BASH_SILENCE_DEPRECATION_WARNING=1

    if [ -f ~/.bashrc ];
    then source ~/.bashrc
    fi

#Step 3: Open your .bashrc and paste this you can customize your terminal.


    red=$(tput setaf 202);
    yellow=$(tput setaf 172);
    blue=$(tput setaf 86);
    green=$(tput setaf 118);
    bold=$(tput bold);
    reset=$(tput sgr0);

    PS1+="\[${bold}\]\n";
    PS1+="\[${red}\]\u"; # username
    PS1+="\[${white}\] at ";
    PS1+="\[${yellow}\]\h"; # host
    PS1+="\[${white}\] in ";
    PS1+="\[${blue}\]\W"; # working directory
    PS1+="\n";
    PS1+="\[${white}\]\$ \[${reset}\]\[${green}\]";
    export PS1;
