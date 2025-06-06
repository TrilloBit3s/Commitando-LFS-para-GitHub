# Commitando-FLS-para-Blender


Para enviar arquivos do GitDesktop para GitHub via Fls.

### 1 - Instale o Gitbash.
### 2 - Execute-o dentro da pasta "Git Bash here".
### 3 - Digite: "touch .gitattributes".
###	    obs: isso serve para criar uma pasta onde deve ser colado os arquivos FLS.
### 4 - Cole este código dentro do arquivo ".gitattributes" que foi criado dentro da sua pasta. 
### 5 - 


	# Arquivos Blender (armazenados via LFS)
	*.blend filter=lfs diff=lfs merge=lfs -text
	*.blend1 filter=lfs diff=lfs merge=lfs -text
	*.blend2 filter=lfs diff=lfs merge=lfs -text

	# Caches, simulações e arquivos binários relacionados
	*.bphys filter=lfs diff=lfs merge=lfs -text
	*.vdb filter=lfs diff=lfs merge=lfs -text
	*.abc filter=lfs diff=lfs merge=lfs -text

	# Texturas e imagens
	*.png filter=lfs diff=lfs merge=lfs -text
	*.jpg filter=lfs diff=lfs merge=lfs -text
	*.jpeg filter=lfs diff=lfs merge=lfs -text
	*.tga filter=lfs diff=lfs merge=lfs -text
	*.exr filter=lfs diff=lfs merge=lfs -text
	*.hdr filter=lfs diff=lfs merge=lfs -text
	*.tif filter=lfs diff=lfs merge=lfs -text
	*.tiff filter=lfs diff=lfs merge=lfs -text
	*.dds filter=lfs diff=lfs merge=lfs -text
	*.bmp filter=lfs diff=lfs merge=lfs -text
	*.webp filter=lfs diff=lfs merge=lfs -text

	# Arquivos de vídeo
	*.mp4 filter=lfs diff=lfs merge=lfs -text
	*.mov filter=lfs diff=lfs merge=lfs -text
	*.avi filter=lfs diff=lfs merge=lfs -text

	# Arquivos de áudio (caso use)
	*.wav filter=lfs diff=lfs merge=lfs -text
	*.mp3 filter=lfs diff=lfs merge=lfs -text
	*.ogg filter=lfs diff=lfs merge=lfs -text

	# Scripts e arquivos de texto
	*.py text eol=lf
	*.txt text eol=lf
	*.md text eol=lf
	*.json text eol=lf

	# Normalização de final de linha
	* text=auto
	
	
### 6 - Salve e volte ao GitDesktop, agora faça o Commit

---------------------------------------------------------------------------------------------------------------------
# Commitando-FLS-para-Unity

Para enviar arquivos do GitDesktop para GitHub via Fls.

### 1 - Instale o Gitbash.
### 2 - Execute-o dentro da pasta "Git Bash here".
### 3 - Digite: "touch .gitattributes".
###	    obs: isso serve para criar uma pasta onde deve ser colado os arquivos FLS.
### 4 - Cole este código dentro do arquivo ".gitattributes" que foi criado dentro da sua pasta. 
### 5 - 

	## Unity ##
	*.cs diff=csharp text
	*.cginc text
	*.shader text
	*.mat merge=unityyamlmerge eol=lf
	*.anim merge=unityyamlmerge eol=lf
	*.unity merge=unityyamlmerge eol=lf
	*.prefab merge=unityyamlmerge eol=lf
	*.physicsMaterial2D merge=unityyamlmerge eol=lf
	*.physicMaterial merge=unityyamlmerge eol=lf
	*.asset merge=unityyamlmerge eol=lf
	*.meta merge=unityyamlmerge eol=lf
	*.controller merge=unityyamlmerge eol=lf

	## git-lfs ##
	# Imagens
	*.jpg filter=lfs diff=lfs merge=lfs -text
	*.jpeg filter=lfs diff=lfs merge=lfs -text
	*.png filter=lfs diff=lfs merge=lfs -text
	*.gif filter=lfs diff=lfs merge=lfs -text
	*.psd filter=lfs diff=lfs merge=lfs -text
	*.ai filter=lfs diff=lfs merge=lfs -text
	*.tif filter=lfs diff=lfs merge=lfs -text

	# Áudio
	*.mp3 filter=lfs diff=lfs merge=lfs -text
	*.wav filter=lfs diff=lfs merge=lfs -text
	*.ogg filter=lfs diff=lfs merge=lfs -text

	# Vídeo
	*.mp4 filter=lfs diff=lfs merge=lfs -text
	*.mov filter=lfs diff=lfs merge=lfs -text

	# Modelos 3D
	*.FBX filter=lfs diff=lfs merge=lfs -text
	*.fbx filter=lfs diff=lfs merge=lfs -text
	*.blend filter=lfs diff=lfs merge=lfs -text
	*.obj filter=lfs diff=lfs merge=lfs -text

	# Outros
	*.a filter=lfs diff=lfs merge=lfs -text
	*.exr filter=lfs diff=lfs merge=lfs -text
	*.tga filter=lfs diff=lfs merge=lfs -text
	*.pdf filter=lfs diff=lfs merge=lfs -text
	*.zip filter=lfs diff=lfs merge=lfs -text
	*.dll filter=lfs diff=lfs merge=lfs -text
	*.unitypackage filter=lfs diff=lfs merge=lfs -text
	*.aif filter=lfs diff=lfs merge=lfs -text
	*.ttf filter=lfs diff=lfs merge=lfs -text
	*.rns filter=lfs diff=lfs merge=lfs -text
	*.reason filter=lfs diff=lfs merge=lfs -text
	*.lxo filter=lfs diff=lfs merge=lfs -text

	
6 - Salve e volte ao GitDesktop, agora faça o Commit
