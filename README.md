# Links

## Snake
https://binofflinessnake.herokuapp.com/

## Gefrierschrank
https://papagefrierschrank.pythonanywhere.com/

## Rezeptbuch
https://mamasrezeptbuch.web.app/

# Free destop in the Browser
first go to https://console.cloud.google.com/?hl=de
click on cloud shell
past the command

docker create \
  --name=webtop \
  -e TZ=Europe/London `# Your local timezone` \
  -e PUID=1000 `# Application user ID you can run the command "id" if you dont know` \
  -e PGID=1001 `# Application group ID same command as above` \
  -v /home/{you're google username}/config `# Application home directory you can run the "pwd" command to and copy the output` \
  -p 8080:3000/tcp `# Web Desktop GUI you dont need to change it` \
  --restart unless-stopped \
  linuxserver/webtop:ubuntu-xfce-version-d94f3c01
 
 and the run "docker start webtop"
 click on web preview and on preview at port 8080
