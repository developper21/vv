import json
import time
import os
from http.server import BaseHTTPRequestHandler, HTTPServer

class AdvanceBypassServer(BaseHTTPRequestHandler):
    
    def get_account_from_file(self, aid):
        # استدعاء ملف الحسابات من المجلد
        file_path = "accounts.json"
        if os.path.exists(file_path):
            with open(file_path, 'r') as f:
                data = json.load(f)
                return data.get(str(aid))
        return None

    def send_payload(self, data):
        payload = json.dumps(data, separators=(',', ':')).encode('utf-8')
        self.send_response(200)
        self.send_header("Content-Type", "application/json")
        self.send_header("Content-Length", str(len(payload)))
        self.end_headers()
        self.wfile.write(payload)

    def do_POST(self):
        # فاش تضغط على Guest Login
        if "/token/grant" in self.path:
            # كنطلبو الحساب رقم 4200764939 من الملف
            acc = self.get_account_from_file(4200764939)
            
            if acc:
                response = {
                    "status": 0,
                    "account_id": 4200764939,
                    "nickname": acc["nickname"], #
                    "level": acc["level"], #
                    "exp": acc["exp"],
                    "coins": acc["coins"], #
                    "gems": acc["gems"],
                    "role": acc["role"], # Admin
                    "region": acc["region"],
                    "access_token": acc["access_token"],
                    "notification_channel": "127.0.0.1:8080",
                    "server_time": int(time.time())
                }
                print(f"✅ Data Loaded from JSON for: {acc['nickname']}")
                self.send_payload(response)
            else:
                self.send_payload({"status": 1, "message": "Account ID not found in JSON"})

    def do_GET(self):
        # كود التحديث (Bypass)
        if "version" in self.path or "ver" in self.path:
            self.send_payload({
                "is_server_open": True,
                "remote_version": "1.10.0",
                "cdn_url": "http://127.0.0.1:8080/",
                "server_url": "http://127.0.0.1:8080/"
            })
        else:
            self.send_payload({"status": 0})

if __name__ == "__main__":
    print("🔥 Server is Running with JSON Database...")
    print("📂 File: accounts.json | Port: 8080")
    server = HTTPServer(("0.0.0.0", 8080), AdvanceBypassServer)
    server.serve_forever()
