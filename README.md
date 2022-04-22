# IrisControls4
Deployed releases of the IrisControls4 application

# Release Notes:

## IrisControls4: 220420<br>


RELEASE_NOTES<br>
	- Support for IC4_v2.3 serial API.<br>
	- Support for displaying unsigned decimal values on FlexSliders.<br>
	- Support for FlexSlider value fields of 10, 12, 14, 18, 22, 26, 30, and 34 digits.<br>
	- Implemented GUI Pages to improve serial connection efficiency when showing or hiding large numbers of elements.<br>
	- Added support for values larger than 2^32 in FlexSlider and FlexDatas.<br>
	- Improved COM menu performance.<br>
	- FlexDatas when disables now clear focus.<br>
	- Multiple value updates for the same element are no longer all sent to the device, only the most recent update is.<br>
	- Improved support for higher resolution displays when plotting data.<br>
=======================================================================<br>

## IrisControls4: 220317<br>

RELEASE_NOTES<br>
	- Clicking on an input FlexSlider or FlexData's label will now bring focus to the value field.<br>
	- While editing a value field, the colours of the field invert. When a value has been accepted and transmitted to the device the colours revert to normal.<br>
	- While editing a value field, an ESC keypress will reject the input and return the value to its last accepted state. The focus on the value field is cleared.<br>
	- While editing a value field, an ENTER/RETURN keypress will accept the input. Focus on the value field is retained.<br>
	- Changed revision format to yymmdd from ddmmyy to match other Iris publications.<br>
	- Symbol parsing for Greek letter mu added.<br>
	- Added support for multiple instance logging.<br>
	- Settings are now stored in a different container for each instance.<br>
	- FlexElement update messages now respect half duplex logic for all connection types.<br>
	- Backend efficiency changes.<br>
=======================================================================<br>

## IrisControls4: 140222<br>

RELEASE_NOTES<br>
	- Removed runtime check for float length in float parsing.<br>
	- Fixed bug causing crash on disconnect for some GUIs.<br>
=======================================================================<br>

## IrisControls4: 080222<br>

RELEASE_NOTES<br>
	- Fixed bug where some handshake rejection cases were not exiting the setup method.<br>
	- Fixed bug where saving datasets could cause a crash if the save folder did not exist.<br>
	- Added save plot as pdf to context menu.<br>
	- COM Port numbering now appended to device names in COM select menu in console.<br>
	- Fixed bug where Windows font scaling was breaking the GUI.<br>
	- Fixed bug where users could not change the baudrate and then change it back again without closing and re-opening the settings dialog.<br>
	- Added error counters and print function (\"errors\") command.<br>
	- Added option to keep Iris Controls 'always on top' in the settings dialog.<br>
	- Added option to auto-reconnect on timeout.<br>
	- Added option to prepend every console message with a timestamp.<br>
	- Element instances and types can now have their colours reset.<br>
	- Local parser can now accept arguments following a command (e.g. the baudrate command).<br>
	- Added debugging logging to the settings dialog.<br>
	- All checkbox settings are now persistent across sessions.<br>
	- Implemented API for setting main window title by device.<br>
	- Added symbol parsing for the copywrite symbol.<br>
=======================================================================<br>

## IrisControls4: 061221<br>

RELEASE_NOTES<br>
	- Update to support IC4 Library v2.0.<br>
	- Added context menu to FlexPlots.<br>
	- Fixed bug where clicking com select menu was causing a crash.<br>
	- Fixed bug where handshake was failing repeatedly.<br>
=======================================================================<br>

## IrisControls4: 211021<br>

RELEASE_NOTES<br>
	- Fixed bug where changing the default colour of a FlexData's units wasn't working.<br>
	- Fixed bug where setting max size of a Dataset was being ignored.<br>
	- Fixed bug where requesting a Dataset without an assigned Flexplot to hide was causing a crash.<br>
=======================================================================<br>

## IrisControls4: 210929<br>

RELEASE_NOTES<br>
	- Fixed bug where configuring FlexLabels was not working.<br>
	- Updated device wide CRC functionality to match the IC4 Library.<br>
	- Added clearer language to the connection log during a device initiated disconnect.<br>
	- Fixed bug where the main window expanded wider and taller than it needed to upon setting new row/column totals.<br>
	- Fixed bug where the traffic display was overlapping itself sometimes.<br>
	- Double clicking FlexPlots toggles user mouse control.<br>
	- Added colour change API for FlexPlot gridlines.<br>
=======================================================================<br>

## IrisControls4: 210914<br>

RELEASE_NOTES<br>
	- Changed the help command for the local parser to \"help\".<br>
	- Added support for console colour change.<br>
	- Font size API implemented.<br>
	- Refined appearance of connection status plot.<br>
	- Added method to set the range (min/max values) of FlexSliders.<br>
	- Changed the way focus works. Tabbing through an application will no longer grant focus to buttons or input only elements.<br>
	- Added keyboard shortcut API.<br>
	- Defined console fonts explicitly to prevent errors with Windows scaling.<br>
=======================================================================<br>


## IrisControls4: 210828<br>

RELEASE_NOTES<br>
	- Added numerical system config to FlexSliders.<br>
	- Fixed bug where hidden datasets were still being plotted in the background.<br>
	- Added support for walking plot domain not defined by a number of datapoints but by the range of those data points.<br>
	- Improved backend plotting efficiency.<br>
	- Fixed bug where FlexPlot x-axis labels were crowding to the point you couldn't read them.<br>
	- Added support for aligning FlexData values left or center.<br>
	- Fixed bug where reconfiguring an element with a different level of precision was not being reflected until the value changed.<br>
	- Removed plot_dataset function in favour of keeping only show and hide functions.<br>
	- FlexPlot axes labels no longer recolour themselves to match their respective dataset.<br>
=======================================================================<br>

## IrisControls4: 210818<br>

RELEASE_NOTES<br>
	- FPS plot in console now has transparent background.<br>
	- Toggling FPS plot in console now auto scrolls the console to the bottom.<br>
	- FlexSliders and FlexDatas can now be configured to hold fewer characters in their value fields.<br>
	- When parsing a string (e.g. element name, units field, etc...) \"*deg*\" will be parsed as a degree symbol and \"*degC*\" will be parsed as degrees Celsius symbol.<br>
	- Added alpha symbol to parsing.<br>
	- Fixed bug where baud rate wasn't changing properly when commanded.<br>
	- Added new baudrates to settings dialog and removed restrictions on manual baudrate entry.<br>
	- Fixed bug where the DIGITS_4 config option for FlexSliders wasn't working.<br>
	- FlexDatas may now be configured to display their values in binary or hexadecimal format. While in either of these modes, users may input values in decimal, binary, or hex by using notation (e.g. '0b123' or '0x123ABC').<br>
	- Fixed bug where non-integer user entered values were being integer rounded before transmission to the device (e.g. 0.5 was being sent as 0).<br>
=======================================================================<br>

## IrisControls4: 210806<br>

RELEASE_NOTES<br>
	- Default colours are now reset upon each new successful serial connection.<br>
	- Devices can now command all default colours to be reset remotely.<br>
	- Setting default colours is now guaranteed to be processed in the same order the serial command to do so is received.<br>
=======================================================================<br>

## IrisControls4: 210804

RELEASE_NOTES<br>
	- Added ability to set colours for disabled state of FlexButtons.<br>
	- Added mirrored FlexSlider and FlexData configurations.<br>
	- Changed traffic display text from \"up\" and \"down\" to up and down arrows.<br>
	- Minimum Console column span reduced to 18 columns.<br>
	- Using \"degC\" in the units field now parses to the degrees Celsius symbol.<br>
	- Fixed problem where setting default FlexSlider colour was affecting the wrong element.<br>
	- Added change colour support for FlexData units field.<br>
	- Fixed bug where FlexPlots weren't respecting the 3 x-axis tick limit resulting in overcrowded labels.<br>
	- Increased size of value field in FlexSliders and FlexDatas to fit six digits and a decimal (up from just 6 digits).<br>

=======================================================================<br>
## IrisControls4: 210726

RELEASE_NOTES <br>
	- Added ability to set colours for disabled state of FlexButtons.<br>
	- Fixed bug where changing checked/unchecked or enabled/disabled states of FlexButtons was not causing the correct colours to be present.<br>
	- Config flag added FlexLabels that sets text alignment.<br>
	- Output Flex Sliders and FlexDatas no longer report new values back to the device.<br>
=======================================================================<br>

## IrisControls4: 210725

RELEASE_NOTES<br>
	- Setting default colours is now live. See wiki for details.<br>
	- Adjusted scaling of the traffic and FPS plot so they aren't drawn on top of each other as often.<br>
	- Changed the way parsing strings is handled to allow users to include whitespace in element names.<br>
=======================================================================<br>

## IrisControls4: 210625

RELEASE_NOTES<br>
	- Added hover_background_normal and hover_background_checked colours to colour change API.<br>
	- Added "release_notes" console command.<br>
	- Fixed missing gear icon in settings dialog button.<br>


=======================================================================<br>

## IrisControls4: 210621

RELEASE_NOTES<br>
	- Added a settings dialog that allows users to configure the baudrate and console output size limit, load config files, and set default settings.<br>
	- Settings dialog is accessed via the gear icon in the top right corner of the console.<br>
	- Baudrate and console output size limit settings are retained across sessions.<br>
	- Console size limit refers to the max number of blocks of text in the output window.If the limit is reached, the output works does a FIFO removal of messages to stay at the limit.<br>
	- "guide_on" and "guide_off" console commands toggle the development grid buttons on and off.The default setting is off but any change is retained across sessions.<br>
	- "max_size" console command displays the max number of rows and columns in the console.<br>
	- Fixed bug where console wasn't scrolling to bottom after every new message.<br>
	- Backend changes to accommodate changes to IC4 library with respect to denominators and decimal places in FlexSliders and FlexDatas.<br>
	- Fixed bug where changing colours of FlexPlots wasn't being reflected until after a new datapoint was added to that FlexPlot.<br>
	- Fixed bug where the Dataset::SCATTER_PLOT config option was being ignored on the first add call for that Dataset.<br>
	- Handshakes can now be received across two USB transmissions(as long as they are not separated by more than the duration of the handshake timer, 500ms)<br>

