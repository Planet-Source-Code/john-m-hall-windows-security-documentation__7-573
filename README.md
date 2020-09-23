<div align="center">

## Windows Security Documentation


</div>

### Description

This document provides information about the Windows security system and what restrictions you can use to limit its functionality.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[John M\. Hall](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/john-m-hall.md)
**Level**          |Intermediate
**User Rating**    |4.7 (61 globes from 13 users)
**Compatibility**  |Delphi 5, Delphi 4, Pre Delphi 4
**Category**       |[Registry](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/registry__7-36.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/john-m-hall-windows-security-documentation__7-573/archive/master.zip)





### Source Code

<P><FONT face=Arial><STRONG><FONT size=6>Windows Security
Documentation<BR></FONT></STRONG><FONT style="FONT-SIZE: 12pt"
color=#000000>Written by John Hall</FONT></FONT><BR><BR><FONT
style="FONT-SIZE: 16pt" face=Arial color=#000000><B>Documentation
Notes</B></FONT></P>
<UL><FONT style="FONT-SIZE: 10pt" face=Arial color=#000000>
 <LI><B>Improvements</B> - Originally, I released this documentation in a
 format that was a little odd/wild, so, as requested, I've cleaned it up and
 added more notes about using it. Hopefully this new organization and these
 notes will help you better understand how to use this information and its
 limitations. I, however, have not added any additional information to this
 documentation because of the limited amount of security information that is
 redily available for the newer operating systems.
 <LI><B>Known Limitations</B> - This information does have some limitations of
 use. Those are mentioned below:
 <UL>
  <LI><B>Operating Systems</B> - This information will most likely <B>not</B>
  work with Microsoft Windows XP or Millennium Edition. It's not been tested,
  so I don't recommend trying it. It's known that a lot of this doesn't work
  with Microsoft Windows NT 4.0 and below, so I also don't recommend its
  application there. If you do decide to try to use it, remember, I'm not
  responsible for your actions and you are doing this on your own accord.
  <LI><B>Setting Overrides</B> - Some settings, none that are noted, have been
  known to override other settings on certain operating systems. This is most
  likely because Microsoft didn't spend the required amount of time making the
  Windows 98 security system(probably the most vulnerable to this problem) a
  high-performance or very reliable work. If you find that some of these
  settings have "holes" or something and it bothers you, I suggest you switch
  to a more securified operating system in the Windows class, such as
  Microsoft Windows 2000 Professional or greater. </LI></UL>
 <LI><B>Special Information</B> - I've reviewed the comments that were posted
 on the original copy of this documentation and this section is here to answer
 some of the questions that I noticed.
 <UL>
  <LI><B>Disabling these Settings</B> - To disable any of the settings that
  are shown in this documentation, simply reverse your process. Just delete
  anything that you added to lock or disable a feature or you can make the
  value the inverse. If it's a DWORD value, make it "00000000" instead of
  "00000001", or a string value "yes" instead of "no" or vice versa.
  <LI><B>Blocking Internet Applications</B> - To disable an application's
  internet access, I suggest you download any free firewall available. A
  firewall will monitor what information is sent and recieved to your computer
  through any network connection and filter it according to rules. The most
  popular, free firewall that is available is <A
  onmouseover="self.status=title;return 0"
  title="Click here to view the ZoneAlarm free edition homepage"
  onmouseout="self.status='';return 0"
  href="http://www.zonealarm.com/products/za/freedownload2.html"
  target=_zonelabs><B>ZoneAlarm</B></A>, by ZoneLabs, Inc. It's actually the
  most secure when it comes to application internet access prevention.
  <LI><B>Reversing Application Lock</B> - As far as I know, there's not a way
  to reverse the application locking method. You might want to experiment with
  it by making a seperate user account on your computer and applying the
  settings to that user only. Basically, that's what I did throughout the
  period that I wrote this documentation and it doesn't harm any of your stuff
  and it helps you uncover the truth. Don't afraid to be creative with this
  information, just remember my disclaimer about it from
above.</LI></UL></LI></UL>
<P><BR><FONT style="FONT-SIZE: 16pt" face=Arial color=#000000><B>Windows System
Security Settings</B></FONT><BR><FONT style="FONT-SIZE: 10pt" face=Arial
color=#000000>All the information that is included in this section affects the
main Windows system. These alter actual system functions and/or settings that it
uses to display certain items.</FONT> </P>
<UL><FONT style="FONT-SIZE: 10pt" face=Arial color=#000000>
 <LI><B>Disable Wallpaper Change</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoChangingWallPaper</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001) </LI></UL><BR>
 <LI><B>Disable All Active Desktop Changes</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoActiveDesktopChanges</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable All Desktop Icons</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDesktop</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Active Desktop</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoActiveDesktop</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable HTML Wallpaper</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoHTMLWallPaper</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Closing Active Desktop Components</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoClosingComponents</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Deleting Active Desktop Components</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoDeletingComponents</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Editing Active Desktop Components</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoEditingComponents</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Adding Active Desktop Components</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\ActiveDesktop\<FONT
  color=#c00000>NoAddingComponents</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Desktop Internet Icon</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoInternetIcon</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Desktop Network Neighborhood Icon</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoNetHood</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Disk Drive Autorun</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDrvieTypeAutoRun</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0xb5000000)</LI></UL><BR>
 <LI><B>Disable Environment Appearance Properties Access</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDispAppearancePage</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Desktop Background Properties Access</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDispBackgroundPage</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Display Icon from Control Panel</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDispCPL</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Screen Saver Properties Access</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>NoDispScrSavPage</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable All But Selected Applications from Running</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\Explorer\<FONT
  color=#c00000>RestrictRun</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)<BR>
  <LI><B>Special Notes</B> - For this setting to work, you will need to make a
  list of programs that you want to allow to run. You can do this by creating
  a Key inside the Explorer Key and calling it RestrictRun and adding string
  values as demonstrated below:
  <UL>
   <LI><B>String Value</B><BR>Name "1"<BR>Value "mspaint.exe"<BR><I><FONT
   color=#008000>This will allow any program named mspaint.exe to run on the
   system</FONT></I><BR>
   <LI><B>String Value</B><BR>Name "2"<BR>Value "iexplore.exe"<BR><I><FONT
   color=#008000>This will allow any program named iexplore.exe to run on the
   system</FONT></I> </LI></UL></LI></UL><BR>
 <LI><B>Disable Start Menu Shut Down Command</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoClose</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Start Menu Log Off Command</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoLogoff</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Start Menu Find Command</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoFind</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Start Menu Documents Menu</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoRecentDocsMenu</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Start Menu Favorites Menu</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoFavoritesMenu</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Settings Menu Folder Options</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoFolderOptions</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Desktop Update</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoDesktopUpdate</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Settings Menu Active Desktop Settings</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoSetActiveDesktop</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Settings Menu Folder Settings</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoSetFolders</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Settings Menu Taskbar Settings</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoSetTaskbar</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Saving Changed Settings</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoSaveSettings</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Right-Click on the Taskbar</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoTrayContextMenu</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Right-Click on the Desktop</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\<FONT
  color=#c00000>NoViewContextMenu</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Microsoft Office Tune Up</B><BR><I><FONT color=#008000>This
 <B>only</B> applies to Microsoft Office 2000</FONT></I>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\Office\9.0\Common\TuneUp\<FONT
  color=#c00000>Disabled</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable AutoComplete in Explorer</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Explorer\AutoComplete\<FONT
  color=#c00000>Use</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of
"no")</LI></UL><BR></LI></UL>
<P><BR><FONT style="FONT-SIZE: 16pt" face=Arial color=#000000><B>Internet
Explorer System Settings</B></FONT><BR><FONT style="FONT-SIZE: 10pt" face=Arial
color=#000000>All the information that is included in this section affects the
operation of Internet Explorer. Please note that these <B>only</B> affect
Internet Explorer's operation and will not work with any other browsers that may
be installed on your computer.</FONT> </P>
<UL><FONT style="FONT-SIZE: 10pt" face=Arial color=#000000>
 <LI><B>Disable Closing Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoBrowserClose</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Right-Click in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoBrowserContextMenu</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Options in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoBrowserOptions</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Saving Pages in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoBrowserSaveAs</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Favorites in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoFavorites</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable File Menu New Object in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoFileNew</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable File Menu Open Object in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoFileOpen</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Finding Files in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoFindFiles</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Opening Files in New Window from Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoOpenInNewWnd</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Selectable Download Directory in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoSelectDownloadDir</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Viewing in Theater Mode in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoTheaterMode</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Viewing Source in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Restrictions\<FONT color=#c00000>NoViewSource</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Adding Channels in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Infodelivery\Restrictions\<FONT
  color=#c00000>NoAddingChannels</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Adding Subscriptions in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Infodelivery\Restrictions\<FONT
  color=#c00000>NoAddingSubscriptions</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Removing Channels in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Infodelivery\Restrictions\<FONT
  color=#c00000>NoRemovingChannels</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Removing Subscriptions in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Infodelivery\Restrictions\<FONT
  color=#c00000>NoRemovingSubscriptions</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Search Customization in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Infodelivery\Restrictions\<FONT
  color=#c00000>NoSearchCustomization</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Running the Connection Wizard</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Control Panel\Restrictions\<FONT color=#c00000>Connwiz Admin
  Lock</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Importing or Exporting Favorites in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\<FONT color=#c00000>DisableImportExportFavorites</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Using the Microsoft Script Debugger in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>Disable Script Debugger</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "yes")</LI></UL><BR>
 <LI><B>Disable Using AutoComplete Forms in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>Use FormSuggest</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL><BR>
 <LI><B>Disable Using AutoComplete Passwords in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>FormSuggest Passwords</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL><BR>
 <LI><B>Disable Using Download Notification in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>NotifyDownloadComplete</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL><BR>
 <LI><B>Disable Error Notification in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>Err Dlg Displayed On Every Error</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL><BR>
 <LI><B>Disable Go Button in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>ShowGoButton</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL><BR>
 <LI><B>Disable Using a Custom Search Page in Web Browser</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>Use Custom Search URL</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000000)</LI></UL><BR>
 <LI><B>Disable Custom Title for Web Browser Windows</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_CURRENT_USER\Software\Microsoft\Internet
  Explorer\Main\<FONT color=#c00000>Window Title</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "custom title
 text")</LI></UL><BR>
 <LI><B>Disable Installation of ISP Distribution Kit for Internet
 Explorer</B><BR><I><FONT color=#008000>This <B>only</B> applies to Internet
 Explorer 5.0 and up</FONT></I>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\Internet
  Connection Wizard\<FONT color=#c00000>CanInstallISPKit5</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of
"no")</LI></UL><BR></LI></UL>
<P><BR><FONT style="FONT-SIZE: 16pt" face=Arial color=#000000><B>Windows Media
Player System Settings</B></FONT><BR><FONT style="FONT-SIZE: 10pt" face=Arial
color=#000000>All the information that is included in this section affects the
operation of Windows Media Player and components. Please note that these
<B>only</B> affect Windows Media Player's operation and will not work with any
other players that may be installed on your computer.</FONT> </P>
<UL><FONT style="FONT-SIZE: 10pt" face=Arial color=#000000>
 <LI><B>Disable Finding New Stations in Media Player</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsMediaPlayer\<FONT
  color=#c00000>NoFindNewStations</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Media Favorites from Media Player</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsMediaPlayer\<FONT
  color=#c00000>NoMediaFavorites</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Radio Bar for Media Player</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\WindowsMediaPlayer\<FONT
  color=#c00000>NoRadioBar</FONT>
  <LI><B>Data Type</B><BR><B>DWORD</B> (set value of 0x00000001)</LI></UL><BR>
 <LI><B>Disable Media Player Upgrade Message</B>
 <UL>
  <LI><B>Location</B><BR>HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\PlayerUpgrade\<FONT
  color=#c00000>AskMeAgain</FONT>
  <LI><B>Data Type</B><BR><B>String</B> (set value of "no")</LI></UL></LI></UL>
<P>&nbsp;</P></FONT></FONT></FONT></FONT>

