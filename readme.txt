Author: Rafa Cobreros rafacobreros@gmail.com
License: GPL
Original theme in: http://gnome-look.org/content/show.php/MediterraneanNight?content=148398

Customization tips:
1.- Style for nautilus
2.- Style for titlebar buttons
3.- Style for tabs
4.- Fix synaptic buttons
5.- Enable/disable the use of the images .svg in checkbox/radiobuttons (GTK2)

---------------------------------
* 1.- Select style for nautilus *
---------------------------------
Edit (gedit) the file ../MediterraneanDark/gtk-3.0/gtk.css

go to the last line of the file, there are three options for nautilus:

	1.- "gnome-applications-gray.css"  		(nautilus sidebar and toolbar dark gray )
	2.- "gnome-applications-unity.css" 		(nautilus sidebar and toolbar dark gray for UNITY)
	3.- "gnome-applications-light.css" 		(nautilus sidebar and toolbar light)
	4.- "gnome-applications-gray-light.css" (nautilus sidebar dark gray and toolbar light)
	
edit (please carefully) the corresponding line "@import" according to the style of nautilus you want,
to make it ONE of the four (not both)

@import url("gnome-applications-gray.css");
or
@import url("gnome-applications-unity.css");
or 
@import url("gnome-applications-light.css");
or
@import url("gnome-applications-gray-light.css");

-----------------------------------------
* 2.- Select style for titlebar buttons *
-----------------------------------------
If you prefer the buttons glassy style for titlebar (apple style):

Copy the contents of the file "metacity_buttons_glassy.tar.gz" in folder .. /MediterraneanDark/metacity-1/

To restore the previous:

Copy the contents of the file "metacity_buttons_normal.tar.gz" in folder .. /MediterraneanDark/metacity-1/

idem for unity buttons
copy the contents of unity_buttons_glassy.tar.gz in folder .. /MediterraneanDark/unity/
or
copy the contents of unity_buttons_normal.tar.gz in folder .. /MediterraneanDark/unity/

NOTE:
	- should close and open session after the changes

------------------------------
* 3. - Select style for TABS *
------------------------------
Edit (gedit) the file ../MediterraneanDark/gtk-3.0/gtk.css

Go to the line where it says
@import url("tabs-dark.css");

and modify it according to the option you want

1.- tabs dark gray (full)
@import url("tabs-dark.css");

2.- tabs themed blue (full)
@import url("tabs-themed.css");

3.- tabs with  blue highlight 
@import url("tabs.css");

4.- tabs with dark gray highlight
@import url("tabs-mono.css");

5.- more traditional style tabs
@import url("tabs-classic.css");

(Be careful to leave only ONE of the five)


-------------------------------------
* 4.- Fix synaptic and GIMP buttons *
-------------------------------------
Note: I have not set by default because sacrifices appearance/quality of the radio-buttons in gtk2.

Edit (gedit) file:
/MediterraneanDark/gtk-2.0/gtkrc

Find the line (near end, about line 860):
widget_class "*<GtkRadioButton>*"				style:highest "radiobutton"

and replaced by:
widget_class "*<GtkRadioButton>*"				style:highest "checkradio"

------------------------------------------------------------------------
* 5.- Enable/disable the use of the images .svg in checkbox/radiobuttons
------------------------------------------------------------------------
Edit (gedit) file:
/MediterraneanDark/gtk-2.0/gtkrc

Find the section (near end, about line 860) and follow the instructions
##########################################################################
# Radiobutton and Checkbox
##########################################################################
# If you have problems displaying the checkbox or radio buttons in gtk2
# uncomment the two lines following (remove the # symbol of the beginning of the line)
# widget_class "*<GtkCheckButton>*"				style "checkradio"
# widget_class "*<GtkRadioButton>*"				style "checkradio"

# and comment on these (put the # symbol at the beginning of the line)
 widget_class "*<GtkCheckButton>*"				style "checkbutton"
 widget_class "*<GtkRadioButton>*" 				style "radiobutton"
##########################################################################


