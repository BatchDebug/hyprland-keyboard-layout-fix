# Hyprland Keyboard Layout Fix
 Keyboard layout not working in Hyperland? Here's how to fix it! 
```
LANGUAGE="de"; [ ! -f ~/.config/hypr/hyprland.conf ] && touch ~/.config/hypr/hyprland.conf && echo '# Hyprland Configuration' >> ~/.config/hypr/hyprland.conf; grep -q 'exec-once=.*setxkbmap' ~/.config/hypr/hyprland.conf && sed -i "s/exec-once=.*setxkbmap.*/exec-once=setxkbmap $LANGUAGE/" ~/.config/hypr/hyprland.conf || echo -e "\nexec-once=setxkbmap $LANGUAGE" >> ~/.config/hypr/hyprland.conf && echo "Keyboard layout set to $LANGUAGE. Please restart Hyperland for changes to take effect."'
```
