let handler = async (m, { isOwner, isAdmin, conn, participants, args }) => {
    if (!(isAdmin || isOwner)) {
        global.dfail('admin', m, conn);
        throw false;
    }

    // نص المنشور المزخرف
    let teks = `🎉🎉【 *⏎ مـــنشـــن«✅» جـــمـــاعـــي* 】🎉🎉\n\n`;
    teks += `💎✨ *「 𝓐𝓱𝓵𝓪𝓷 𝓬𝓸𝓶𝓮 𝓮𝓿𝓮𝓻𝓎𝓸𝓷𝓮 」* ✨💎\n\n`;

    for (let mem of participants) {
        teks += `⚡ *• 𝑯𝑬𝑳𝑳𝑶 @${mem.id.split('@')[0]}* ⚡\n`;
    }

    teks += `\n🖤✴️ *❂━━━━━━━━━━━━━━━━━❂* ✴️🖤\n`;
    teks += `🌟 *𝐁𝐋𝐀𝐂𝐊 𝐁𝐎𝐓 ﴾𝟎𝟏𝟓𝟓𝟒𝟏𝟗𝟔𝟒𝟒𝟓﴿* 🌟\n`;
    teks += `✨ *⚡ شكرًا لكم على المشاركة الرائعة ⚡* ✨`;

    // إرسال الرسالة مع المنشن
    conn.sendMessage(
        m.chat,
        { text: teks, mentions: participants.map(a => a.id) },
        {}
    );
};

handler.help = ['tagall <message>', 'invocar <message>'];
handler.tags = ['group'];
handler.command = /^(منشن|invocar|invocacion|todos|invocación)$/i;

handler.admin = true;
handler.group = true;

export default handler;
