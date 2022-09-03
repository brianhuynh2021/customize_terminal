# customize_terminal
-- Open your .bashrc and paste this you can customize your terminal

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
