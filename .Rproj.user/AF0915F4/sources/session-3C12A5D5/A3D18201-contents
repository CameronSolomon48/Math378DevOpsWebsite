from vetiver import VetiverModel
from dotenv import load_dotenv, find_dotenv
import vetiver
import pins

load_dotenv(find_dotenv())

b = pins.board_folder('data/model', allow_pickle_read=True)
v = VetiverModel.from_pin(b, 'penguin_model', version = "20240312T094249Z-a6f9b")

vetiver_api = vetiver.VetiverAPI(v)
app = vetiver_api.app

if __name__ == "__main__":
  import uvicorn
  uvicorn.run(app, host = "127.0.0.1", port = 8080)
  
