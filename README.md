from datetime import datetime
import pytz

kenya_tz = pytz.timezone("Africa/Nairobi")
kenya_time = datetime.now(kenya_tz)

print("Kenya Time:", kenya_time.strftime("%H:%M:%S"))
