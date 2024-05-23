import discord
from discord.ext import commands
import random
import os
print(os.listdir('images'))

intents = discord.Intents.default()
intents.message_content = True

sonuc = ("SİYAH", "KIRMIZI", "YEŞİL")

bot = commands.Bot(command_prefix='$', intents=intents)

@bot.event
async def on_ready():
    print(f'{bot.user} olarak giriş yaptık')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Merhaba! Ben {bot.user}, bir Discord sohbet botuyum!')

@bot.command()
async def heh(ctx, count_heh = 5):
    await ctx.send("he" * count_heh)

@bot.command()
async def nasilimm(ctx):
    await ctx.send("FaÇaSıN kArDeŞiM bEnİm DiKkAt Et KeSmE bİzİ hA")
    
@bot.command()
async def bye(ctx):
    await ctx.send("baysssss :3 :3 :3")
       
@bot.command()
async def rulet(ctx, karar: str):
    secilen_renk = random.choice(sonuc)
    
    if secilen_renk == karar:
        await ctx.send("Tebrikler Tahmininiz Doğru :)")
    else:
        await ctx.send(f"Maalesef Kaybettiniz :(, Cevap {secilen_renk} Olmalıydı")
        
@bot.command()
async def mem(ctx):
    with open('images/a1.png', 'rb') as f:
        picture = discord.File(f)

    await ctx.send(file=picture)
    
@bot.command()
async def mem2(ctx):
    with open('images/a2.png', 'rb') as f:
        picture = discord.File(f)

    await ctx.send(file=picture)

@bot.command()
async def mem3(ctx):
    with open('images/a3.png', 'rb') as f:
        picture = discord.File(f)

    await ctx.send(file=picture)
    
@bot.command()
async def mem4(ctx):
    with open('images/a4.jpeg', 'rb') as f:
        picture = discord.File(f)

    await ctx.send(file=picture)
    
@bot.command()
async def mem5(ctx):
    with open('images/a5.jpeg', 'rb') as f:
        picture = discord.File(f)

    await ctx.send(file=picture)
 
img_name = "a2.png"
    
@bot.command()
async def randommem(ctx):
    with open(f'images/{img_name}', 'rb') as f:
        picture = discord.File(f)
    await ctx.send(file=picture)
    
@bot.command()
async def kekomem(ctx):
    with open('images/a4.jpeg', 'rb') as f:
        picture = discord.File(f)
        
    await ctx.send(file=picture)
    await ctx.send("KuLa GüVeNeN yOlDa KaLıR ALLAH'A gÜvEnEn YoL aLıR, HaYıRlI CuMalAr")
    
cozumler = [
    "Atık malzemeleri kullanarak ev dekorasyonu veya el sanatları yapmak", 
    "Bez Torbalar ve Alışveriş Çantaları Kullanın", 
    "Daha Az Ambalajlı Ürünleri Tercih Edin", 
    "Tek Kullanımlık Ürünleri Kullanmayın", 
    "Yeniden Kullanılabilir Malzemeler Edinin"
]

@bot.command()
async def cozum(ctx):
    secim = random.choice(cozumler)
    
    await ctx.send(secim) 
    
@bot.command()
async def cozum1(ctx):
    await ctx.send("Sürdürülebilirlik için hangi çözümü istersiniz? Aşağıdaki seçeneklerden birini seçin:\n1. Atık malzemeleri kullanarak ev dekorasyonu veya el sanatları yapmak\n2. Bez Torbalar ve Alışveriş Çantaları Kullanın\n3. Daha Az Ambalajlı Ürünleri Tercih Edin\n4. Tek Kullanımlık Ürünleri Kullanmayın\n5. Yeniden Kullanılabilir Malzemeler Edinin")

    def check(msg):
        return msg.author == ctx.author and msg.channel == ctx.channel

    try:
        msg = await bot.wait_for('message', check=check, timeout=30)
        choice = int(msg.content)
        if 1 <= choice <= 5:
            await ctx.send(cozumler[choice - 1])
        else:
            await ctx.send("Geçersiz seçim. Lütfen 1 ile 5 arasında bir sayı girin.")
    except ValueError:
        await ctx.send("Geçersiz giriş. Lütfen 1 ile 5 arasında bir sayı girin.")

  
bot.run("")
