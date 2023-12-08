Enjoy this preset optimized server files!

Pterodactyl install egg script modification:

```bash
if [ ! -f server.properties ]; then
echo -e "Downloading optimized server.properties"
curl -o server.properties https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/server.properties
fi
if [ ! -f spigot.yml ]; then
echo -e "Downloading optimized spigot.yml"
curl -o spigot.yml https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/spigot.yml
fi
if [ ! -f bukkit.yml ]; then
echo -e "Downloading optimized bukkit.yml"
curl -o bukkit.yml https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/bukkit.yml
fi

number=$(echo ${MINECRAFT_VERSION} | cut -d'.' -f2);
if [ "${MINECRAFT_VERSION}" != "latest" ] && [ "$number" -ge 8 ] && [ "$number" -le 18 ]; then

if [ ! -f paper.yml ]; then
echo -e "Downloading optimized paper.yml (1.8 - 1.18)"
curl -o paper.yml https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/paper.yml
fi

else

mkdir config
if [ ! -f config/paper-global.yml ]; then
echo -e "Downloading optimized paper-global.yml (1.19+)"
curl -o config/paper-global.yml https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/paper-global.yml
fi
if [ ! -f config/paper-world-defaults.yml ]; then
echo -e "Downloading optimized paper-world-defaults.yml (1.19+)"
curl -o config/paper-world-defaults.yml https://raw.githubusercontent.com/Straikerinos/optimized-server-settings/main/paper-world-defaults.yml
fi

fi```
