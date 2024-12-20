const { Client, GatewayIntentBits } = require('discord.js');
const client = new Client({ intents: [GatewayIntentBits.Guilds, GatewayIntentBits.GuildMessages, GatewayIntentBits.MessageContent] });

const TOKEN = 'MTMxOTc5OTY5ODU1ODU1MDEwOQ.GRvrlT.xvtx8KCK7-E1leFaIwMdDpSOQjtKd7dt9RjPxk'; // Replace this with your bot token

client.once('ready', () => {
    console.log('Bot is online!');
});

client.on('messageCreate', (message) => {
    if (message.content === '!b') {
        message.channel.send('A Discord bot is an application that runs on the Discord platform and can perform automated tasks, respond to commands, and interact with users in a server.');
    }
});

client.login(TOKEN);
