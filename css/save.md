Importing and Exporting Blocks
If your application needs to save and store the user's blocks and restore them at a later visit, use this call for export to XML:

var xml = Blockly.Xml.workspaceToDom(workspace);
var xml_text = Blockly.Xml.domToText(xml);

This will produce a minimal (but ugly) string containing the XML for the user's blocks. If one wishes to obtain a more readable (but larger) string, use Blockly.Xml.domToPrettyText instead.

Restoring from an XML string to blocks is just as simple:

var xml = Blockly.Xml.textToDom(xml_text);
Blockly.Xml.domToWorkspace(xml, workspace);