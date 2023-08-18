
<%*
let templater = app.plugins.plugins["templater-obsidian"];
let templateFolder = templater.settings.templates_folder;

let noteTypes = [
  {format: "house", template: "templates.house.md"},
  {format : "room", template: "room.md"}
];


for (const noteType of noteTypes) {
	var title = tp.file.title;
	var split_title = title.split(".");
	if (split_title[0].includes(noteType.format)){
	  var templateTFile =
            `${templateFolder}/${noteType.template}`
   
	var location = tp.file.find_tfile(templateTFile);
	
	 templater.templater.append_template_to_active_file(
            location
        );
	
	}
}

-%>

