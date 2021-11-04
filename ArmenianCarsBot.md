import types

import telebot
from telebot import types

TOKEN = '2054668897:AAGh_frAuyqYlvt7frVQO_KFj3CV7xnOxk8'
bot = telebot.TeleBot(TOKEN)


@bot.message_handler(content_types=['text'])
def get_text_message(message):
    if message.text == "Привет":
        bot.send_message(message.from_user.id, "Привет!")
    keyboard = types.InlineKeyboardMarkup()
    key_audi = types.InlineKeyboardButton(text='Audi', callback_data='audi')
    keyboard.add(key_audi)
    key_kia = types.InlineKeyboardButton(text='KIA', callback_data='kia')
    keyboard.add(key_kia)
    key_bmw = types.InlineKeyboardButton(text='BMW', callback_data='bmw')
    keyboard.add(key_bmw)
    key_ford = types.InlineKeyboardButton(text='Ford', callback_data='ford')
    keyboard.add(key_ford)
    key_honda = types.InlineKeyboardButton(text='Honda', callback_data='honda')
    keyboard.add(key_honda)
    key_hyundai = types.InlineKeyboardButton(text='Hyundai', callback_data='hyundai')
    keyboard.add(key_hyundai)
    key_landrover = types.InlineKeyboardButton(text='Land Rover', callback_data='landrover')
    keyboard.add(key_landrover)
    key_mercedesbenz = types.InlineKeyboardButton(text='Mercedes-Benz', callback_data='mercedesbenz')
    keyboard.add(key_mercedesbenz)
    key_porsche = types.InlineKeyboardButton(text='Porsche', callback_data='porsche')
    keyboard.add(key_porsche)
    key_toyota = types.InlineKeyboardButton(text='Toyota', callback_data='toyota')
    keyboard.add(key_toyota)
    key_lada = types.InlineKeyboardButton(text='Lada', callback_data='lada')
    keyboard.add(key_lada)
    key_mazda = types.InlineKeyboardButton(text='Mazda', callback_data='mazda')
    keyboard.add(key_mazda)
    key_ferrari = types.InlineKeyboardButton(text='Ferrari', callback_data='ferrari')
    keyboard.add(key_ferrari)
    key_rollsroyce = types.InlineKeyboardButton(text='Rolls Royce', callback_data='rollsroyce')
    keyboard.add(key_rollsroyce)
    key_chevrolete = types.InlineKeyboardButton(text='Chevrolete', callback_data='chevrolete')
    keyboard.add(key_chevrolete)
    bot.send_message(message.from_user.id, text='Choose a brand!', reply_markup=keyboard)


@bot.callback_query_handler(func=lambda call: True)
def callback_worker(call):
    if call.data == "1":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221046%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "2":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221047%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "3":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221048%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "4":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221050%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "5":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221049%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "6":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221051%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "7":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%223817%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "8":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221055%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "9":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2221%22],%22model%22:{%2221%22:[%221056%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "10":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22191%22],%22model%22:{%22191%22:[%223993%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "11":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22191%22],%22model%22:{%22191%22:[%223994%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "12":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22191%22],%22model%22:{%22191%22:[%221726%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "13":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22191%22],%22model%22:{%22191%22:[%221733%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "14":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22191%22],%22model%22:{%22191%22:[%221739%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "15":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%22475%22,%223822%22,%221079%22,%221080%22,%221081%22,%223823%22,%223824%22,%221082%22,%223825%22,%223826%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "16":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%223563%22,%223827%22,%223828%22,%223829%22,%223572%22,%223573%22,%223574%22,%223575%22,%223830%22,%223831%22,%223832%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "17":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%22476%22,%221083%22,%222861%22,%221085%22,%221086%22,%221087%22,%221088%22,%221089%22,%221090%22,%221091%22,%223689%22,%223834%22,%223833%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "18":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%223564%22,%223577%22,%223578%22,%223579%22,%223580%22,%223581%22,%223582%22,%223835%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "19":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%22477%22,%221092%22,%221093%22,%221094%22,%221095%22,%221096%22,%221097%22,%221098%22,%221099%22,%221100%22,%221101%22,%221102%22,%223836%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "20":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%22478%22,%221103%22,%223837%22,%221104%22,%221105%22,%223838%22,%221106%22,%221107%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "21":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%22479%22,%221108%22,%221109%22,%221110%22,%221111%22,%221112%22,%221113%22,%221114%22,%221115%22,%221116%22,%223690%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "22":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%222969%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "23":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%224729%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "24":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%221125%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "25":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%223842%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "26":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%221126%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "27":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%222685%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "28":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2231%22],%22model%22:{%2231%22:[%224725%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "29":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22116%22],%22model%22:{%22116%22:[%221470%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "30":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22116%22],%22model%22:{%22116%22:[%221472%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "31":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22116%22],%22model%22:{%22116%22:[%221480%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "32":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22116%22],%22model%22:{%22116%22:[%221494%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "33":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22146%22],%22model%22:{%22146%22:[%221541%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "34":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22146%22],%22model%22:{%22146%22:[%221549%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "35":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22146%22],%22model%22:{%22146%22:[%221551%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "36":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22146%22],%22model%22:{%22146%22:[%221558%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "37":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22146%22],%22model%22:{%22146%22:[%221576%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "38":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%221596%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "39":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%221602%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "40":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%221618%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "41":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%223721%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "42":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%221620%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "43":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22156%22],%22model%22:{%22156%22:[%221627%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "44":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22206%22],%22model%22:{%22206%22:[%221778%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "45":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22206%22],%22model%22:{%22206%22:[%223498%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "46":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22206%22],%22model%22:{%22206%22:[%223995%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "47":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22206%22],%22model%22:{%22206%22:[%221779%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "48":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22483%22,%221920%22,%221921%22,%221922%22,%221923%22,%221924%22,%221925%22,%221926%22,%221927%22,%224035%22,%224036%22,%224037%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "49":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22484%22,%221928%22,%224113%22,%221929%22,%221930%22,%221931%22,%224038%22,%224039%22,%224040%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "50":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22485%22,%221937%22,%221938%22,%221939%22,%221940%22,%221941%22,%221942%22,%221943%22,%221944%22,%221945%22,%221932%22,%222947%22,%221933%22,%221946%22,%221947%22,%221934%22,%224114%22,%221935%22,%224115%22,%221936%22,%223496%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "51":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22491%22,%221982%22,%221983%22,%221984%22,%221985%22,%221986%22,%221987%22,%221988%22,%221989%22,%221990%22,%221991%22,%221992%22,%221993%22,%221977%22,%221994%22,%221995%22,%221996%22,%221997%22,%224047%22,%221998%22,%221999%22,%221978%22,%224048%22,%222000%22,%221979%22,%224049%22,%222001%22,%221980%22,%224050%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "52":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22500%22,%222063%22,%222064%22,%222065%22,%224106%22,%222066%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "53":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%223560%22,%223565%22,%223566%22,%223567%22,%223568%22,%223569%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "54":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22490%22,%224043%22,%224044%22,%222957%22,%224045%22,%221974%22,%221975%22,%224046%22,%221976%22,%221972%22,%223590%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "55":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%223739%22,%224057%22,%224058%22,%224059%22,%224060%22,%224061%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "56":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%223740%22,%224067%22,%224068%22,%224069%22,%224070%22,%224071%22,%224072%22,%224073%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "57":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%224079%22,%224080%22,%224081%22,%224082%22,%224083%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "58":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22492%22,%222003%22,%222004%22,%222005%22,%224051%22,%222006%22,%222007%22,%222008%22,%222009%22,%222010%22,%222011%22,%222012%22,%222002%22,%222959%22,%223082%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "59":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22246%22],%22model%22:{%22246%22:[%22495%22,%222019%22,%224084%22,%222020%22,%222021%22,%224085%22,%222022%22,%222023%22,%222024%22,%224086%22,%222025%22,%224087%22,%222026%22,%222017%22,%222018%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "60":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22316%22],%22model%22:{%22316%22:[%222322%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "61":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22316%22],%22model%22:{%22316%22:[%222331%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "62":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22316%22],%22model%22:{%22316%22:[%222332%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "63":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22316%22],%22model%22:{%22316%22:[%222335%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "64":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22316%22],%22model%22:{%22316%22:[%223583%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "65":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222517%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "66":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222520%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "67":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222531%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "68":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222532%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "69":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222542%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "70":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22386%22],%22model%22:{%22386%22:[%222535%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "71":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2256%22],%22model%22:{%2256%22:[%223855%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "72":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%2256%22],%22model%22:{%2256%22:[%221180%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "73":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22106%22],%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "74":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22331%22],%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "75":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22396%22],%22model%22:{%22396%22:[%223597%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "76":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22396%22],%22model%22:{%22396%22:[%222967%22,%222968%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == "77":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%221862%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "78":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%221864%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "79":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%224034%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "80":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%223545%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "81":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%221878%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)
    if call.data == "82":
        msg = 'https://auto.am/search/passenger-cars?q={%22category%22:%221%22,%22page%22:%221%22,%22sort%22:%22latest%22,%22layout%22:%22list%22,%22user%22:{%22dealer%22:%220%22,%22id%22:%22%22},%22make%22:[%22241%22],%22model%22:{%22241%22:[%222931%22]},%22year%22:{%22gt%22:%221911%22,%22lt%22:%222022%22},%22usdprice%22:{%22gt%22:%220%22,%22lt%22:%22100000000%22},%22mileage%22:{%22gt%22:%2210%22,%22lt%22:%221000000%22}}'
        bot.send_message(call.from_user.id, msg)

    if call.data == 'audi':
        keyboard = types.InlineKeyboardMarkup()
        key_audi = types.InlineKeyboardButton(text='A3 💥', callback_data='1')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='A4 💥', callback_data='2')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='A5 💥', callback_data='3')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='A6 💥', callback_data='4')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='A7 💥', callback_data='5')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='A8 💥', callback_data='6')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='Q3 💥', callback_data='7')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='Q5 💥', callback_data='8')
        keyboard.add(key_audi)
        key_audi = types.InlineKeyboardButton(text='Q7 💥', callback_data='9')
        keyboard.add(key_audi)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'kia':
        keyboard = types.InlineKeyboardMarkup()
        key_kia = types.InlineKeyboardButton(text='Forte 🔥', callback_data='10')
        keyboard.add(key_kia)
        key_kia = types.InlineKeyboardButton(text='Forte coupe 🔥', callback_data='11')
        keyboard.add(key_kia)
        key_kia = types.InlineKeyboardButton(text='Optima 🔥', callback_data='12')
        keyboard.add(key_kia)
        key_kia = types.InlineKeyboardButton(text='Rio 🔥', callback_data='13')
        keyboard.add(key_kia)
        key_kia = types.InlineKeyboardButton(text='Sorento 🔥', callback_data='14')
        keyboard.add(key_kia)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'bmw':
        keyboard = types.InlineKeyboardMarkup()
        key_bmw = types.InlineKeyboardButton(text='1 series ⚡', callback_data='15')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='2 series ⚡', callback_data='16')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='3 series ⚡', callback_data='17')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='4 series ⚡', callback_data='18')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='5 series ⚡', callback_data='19')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='6 series ⚡', callback_data='20')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='7 series ⚡', callback_data='21')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X1 ⚡', callback_data='22')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X2 ⚡', callback_data='23')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X3 ⚡', callback_data='24')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X4 ⚡', callback_data='25')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X5 ⚡', callback_data='26')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X6 ⚡', callback_data='27')
        keyboard.add(key_bmw)
        key_bmw = types.InlineKeyboardButton(text='X7 ⚡', callback_data='28')
        keyboard.add(key_bmw)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'ford':
        keyboard = types.InlineKeyboardMarkup()
        key_ford = types.InlineKeyboardButton(text='Focus 🪵', callback_data='29')
        keyboard.add(key_ford)
        key_ford = types.InlineKeyboardButton(text='Fusion 🪵', callback_data='30')
        keyboard.add(key_ford)
        key_ford = types.InlineKeyboardButton(text='Mustang 🪵', callback_data='31')
        keyboard.add(key_ford)
        key_ford = types.InlineKeyboardButton(text='Transit 🪵', callback_data='32')
        keyboard.add(key_ford)

    if call.data == 'honda':
        keyboard = types.InlineKeyboardMarkup()
        key_honda = types.InlineKeyboardButton(text='Accord 🐉', callback_data='33')
        keyboard.add(key_honda)
        key_honda = types.InlineKeyboardButton(text='Civic 🐉', callback_data='34')
        keyboard.add(key_honda)
        key_honda = types.InlineKeyboardButton(text='CR-V 🐉', callback_data='35')
        keyboard.add(key_honda)
        key_honda = types.InlineKeyboardButton(text='Fit 🐉', callback_data='36')
        keyboard.add(key_honda)
        key_honda = types.InlineKeyboardButton(text='Pilot 🐉', callback_data='37')
        keyboard.add(key_honda)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'hyundai':
        keyboard = types.InlineKeyboardMarkup()
        key_hyundai = types.InlineKeyboardButton(text='Accent 🫀', callback_data='38')
        keyboard.add(key_hyundai)
        key_hyundai = types.InlineKeyboardButton(text='Elantra 🫀', callback_data='39')
        keyboard.add(key_hyundai)
        key_hyundai = types.InlineKeyboardButton(text='Santa-fe 🫀', callback_data='40')
        keyboard.add(key_hyundai)
        key_hyundai = types.InlineKeyboardButton(text='Solaris 🫀', callback_data='41')
        keyboard.add(key_hyundai)
        key_hyundai = types.InlineKeyboardButton(text='Sonata 🫀', callback_data='42')
        keyboard.add(key_hyundai)
        key_hyundai = types.InlineKeyboardButton(text='Tucson 🫀', callback_data='43')
        keyboard.add(key_hyundai)
        bot.send_message(call.from_user.id, text='Выбери модель!!', reply_markup=keyboard)

    if call.data == 'landrover':
        keyboard = types.InlineKeyboardMarkup()
        key_landrover = types.InlineKeyboardButton(text='Range-Rover 🤘', callback_data='44')
        keyboard.add(key_landrover)
        key_landrover = types.InlineKeyboardButton(text='Range-Rover Evoque 🤘', callback_data='45')
        keyboard.add(key_landrover)
        key_landrover = types.InlineKeyboardButton(text='Range-Rover Velar 🤘', callback_data='46')
        keyboard.add(key_landrover)
        key_landrover = types.InlineKeyboardButton(text='Range-Rover sport 🤘', callback_data='47')
        keyboard.add(key_landrover)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'mercedesbenz':
        keyboard = types.InlineKeyboardMarkup()
        key_mercedesbenz = types.InlineKeyboardButton(text='A class 🦈', callback_data='48')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='B class 🦈', callback_data='49')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='C class 🦈', callback_data='50')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='E class 🦈', callback_data='51')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='V class 🦈', callback_data='52')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='Cla class 🦈', callback_data='53')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='Cls class 🦈', callback_data='54')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='GLA class 🦈', callback_data='55')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='GLE class 🦈', callback_data='56')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='GLS class 🦈', callback_data='57')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='G class 🦈', callback_data='58')
        keyboard.add(key_mercedesbenz)
        key_mercedesbenz = types.InlineKeyboardButton(text='ML class 🦈', callback_data='59')
        keyboard.add(key_mercedesbenz)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'porsche':
        keyboard = types.InlineKeyboardMarkup()
        key_porsche = types.InlineKeyboardButton(text='911 ⚰️', callback_data='60')
        keyboard.add(key_porsche)
        key_porsche = types.InlineKeyboardButton(text='Cayenne ⚰', callback_data='61')
        keyboard.add(key_porsche)
        key_porsche = types.InlineKeyboardButton(text='Cayman ⚰', callback_data='62')
        keyboard.add(key_porsche)
        key_porsche = types.InlineKeyboardButton(text='Panamera ⚰', callback_data='63')
        keyboard.add(key_porsche)
        key_porsche = types.InlineKeyboardButton(text='Macan ⚰', callback_data='64')
        keyboard.add(key_porsche)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'toyota':
        keyboard = types.InlineKeyboardMarkup()
        key_toyota = types.InlineKeyboardButton(text='Camry 🧨', callback_data='65')
        keyboard.add(key_toyota)
        key_toyota = types.InlineKeyboardButton(text='Corolla 🧨', callback_data='66')
        keyboard.add(key_toyota)
        key_toyota = types.InlineKeyboardButton(text='Land Cruiser 🧨', callback_data='67')
        keyboard.add(key_toyota)
        key_toyota = types.InlineKeyboardButton(text='Land Cruiser Prado 🧨', callback_data='68')
        keyboard.add(key_toyota)
        key_toyota = types.InlineKeyboardButton(text='Prius 🧨', callback_data='69')
        keyboard.add(key_toyota)
        key_toyota = types.InlineKeyboardButton(text='RAV 4 🧨', callback_data='70')
        keyboard.add(key_toyota)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'Chevrolet':
        keyboard = types.InlineKeyboardMarkup()
        key_ferrari = types.InlineKeyboardButton(text='Volt 💸', callback_data='71')
        keyboard.add(key_ferrari)
        key_ferrari = types.InlineKeyboardButton(text='Camaro 💸', callback_data='72')
        keyboard.add(key_ferrari)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'ferrari':
        keyboard = types.InlineKeyboardMarkup()
        key_ferrari = types.InlineKeyboardButton(text='Ferrari 💸', callback_data='73')
        keyboard.add(key_ferrari)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'rr':
        keyboard = types.InlineKeyboardMarkup()
        key_rollsroyce = types.InlineKeyboardButton(text='Rolls Royce 💰', callback_data='74')
        keyboard.add(key_rollsroyce)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'lada':
        keyboard = types.InlineKeyboardMarkup()
        key_lada = types.InlineKeyboardButton(text='2121 NIVA 🪵', callback_data='75')
        keyboard.add(key_lada)
        key_lada = types.InlineKeyboardButton(text='Priora 🪵', callback_data='76')
        keyboard.add(key_lada)
        bot.send_message(call.from_user.id, text='Выбери модель!', reply_markup=keyboard)

    if call.data == 'mazda':
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda 3', callback_data='77')
        keyboard.add(key_mazda)
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda 6', callback_data='78')
        keyboard.add(key_mazda)
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda CX3', callback_data='79')
        keyboard.add(key_mazda)
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda CX5', callback_data='80')
        keyboard.add(key_mazda)
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda CX7', callback_data='81')
        keyboard.add(key_mazda)
        keyboard = types.InlineKeyboardMarkup()
        key_mazda = types.InlineKeyboardButton(text='Mazda CX9', callback_data='82')
        keyboard.add(key_mazda)


bot.infinity_polling()
