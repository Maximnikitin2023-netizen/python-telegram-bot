CommandHandler
==============

.. autoclass:: telegram.ext.CommandHandler
    :members:
    :show-inheritance:
from telegram import Update
from telegram.ext import ApplicationBuilder, CommandHandler, ContextTypes

TOKEN = "8727169961:AAGGPrbsn8uRsD8SmyNxL2rWrguuEphGeWk"

async def calc(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("Калькулятор работает!")

app = ApplicationBuilder().token(8727169961:AAGGPrbsn8uRsD8SmyNxL2rWrguuEphGeWk).build()

app.add_handler(CommandHandler("calc", calc))

app.run_polling()
