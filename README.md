# Commitando-LFS-para-Blender


Para enviar arquivos do GitDesktop para GitHub via LFS.

### 1 - Instale o Gitbash.
### 2 - Execute-o dentro da pasta "Git Bash here".
### 3 - Digite: "touch .gitattributes".
###	    obs: isso serve para criar uma pasta onde deve ser colado os arquivos LFS.
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
# Commitando-LFS-para-Unity

Para enviar arquivos do GitDesktop para GitHub via lfs.

### 1 - Instale o Gitbash.
### 2 - Execute-o dentro da pasta "Git Bash here".
### 3 - Digite: "touch .gitattributes".
###	    obs: isso serve para criar uma pasta onde deve ser colado os arquivos LFS.
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
---------------------------------------------------------------------------------------------------------------------
OBs:

Explicação por partes:
GIT_LFS_SKIP_SMUDGE=1
É uma variável de ambiente usada pelo Git LFS (Large File Storage). Ela impede que os arquivos grandes gerenciados pelo LFS sejam baixados automaticamente durante o clone do repositório.

Ou seja: os arquivos LFS serão clonados como "ponteiros" (pequenos arquivos de texto que referenciam os arquivos reais) — economizando tempo e banda no momento do clone.

git clone https://github.com/seu-usuario/Seu-Projeto.git
Esse é o comando padrão para clonar um repositório Git do GitHub.

Na prática:
Você clona o repositório normalmente,

Mas os arquivos LFS (como .png, .psd, .fbx, .blend, etc., se forem controlados pelo Git LFS) não são baixados automaticamente.
---------------------------------------------------------------------------------------------------------------------

### Este código só deve ser usado se exeder o limite do LFS, neste caso vai cancelar o LFS do git.
### Se do contrario, remova remova estes comentario.
### Remover o got git LFS 
---------------------------------------------------------------------------------------------------------------------
# use a linha por inteiro para cancelar o LFS
### GIT_LFS_SKIP_SMUDGE=1 git clone https://github.com/seu-usuario/seu-projeto.git
