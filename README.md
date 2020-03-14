function postMessageToDiscord(message) {

  message = message || "t!fishy";

  var discordUrl = 'https://discordapp.com/api/webhooks/688374765974716460/Q8X_gfR2YDQX_ItWV2QDRSFDiPE5i8AYgh2HjK9rH-Zh2vtSEwP6ei_g7A6w-PBvhIEo';
  var payload = JSON.stringify({content: message});

  var params = {
    headers: {
      'Content-Type': 'application/x-www-form-urlencoded'
    },
    method: "POST",
    payload: payload,
    muteHttpExceptions: true
  };

  var response = UrlFetchApp.fetch(discordUrl, params);

  Logger.log(response.getContentText());

}
