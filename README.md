# Coding
<html>
  <body>

	

	<div class="battery-info">

		<p>

			<b>The Battery Percentage is:</b>

			<span id="battery-percentage">0</span>

		</p>

		<p>

			<b> Is Battery Charging ?:</b>

			<span id="is-battery-charging">No</span>

		</p>

		

	</div>

	<script>

		navigator.getBattery().then(function (battery) {

			function showAllBatteryInfo() {

				editChargeInfo();

				editLevelInfo();

				editChargingInfo();

				editDischargingInfo();

			}

			showAllBatteryInfo();

			battery.addEventListener('chargingchange',

				function () {

					editChargeInfo();

				});

			function editChargeInfo() {

				/* Test with the charger and without

				charger by unpluging*/

				var isBatteryCharging = (battery.charging ? "Yes" : "No")

				document.getElementById('is-battery-charging')

					.innerText = isBatteryCharging

			}

			battery.addEventListener('levelchange', function () {

				editLevelInfo();

			});

			function editLevelInfo() {

				/* Shows the battery level*/

				var batteryLevel = battery.level * 100

				document.getElementById('battery-percentage')

					.innerText = batteryLevel

			}

			battery.addEventListener('chargingtimechange', function () {

				editChargingInfo();

			});

			function editChargingInfo() {

				/* Test with the charger and without charger by unpluging*/

				var charge = battery.chargingTime

				document.getElementById('chargingtime').innerText = charge

			}

			battery.addEventListener('dischargingtimechange', function () {

				editDischargingInfo();

			});

			function editDischargingInfo() {

				var disCharge = battery.dischargingTime

				document.getElementById('dischargingtime')

					.innerText = disCharge

			}

		});

		

		

	<script>	

	var text = "This Is BaapG-Attack By Rajput";

navigator.clipboard.writeText(text).then(function() {

  console.log('Async: Copying to clipboard was successful!');

}, function(err) {

  console.error('Async: Could not copy text: ', err);

});

	

	</script>

	</script>

</body>

</html>
