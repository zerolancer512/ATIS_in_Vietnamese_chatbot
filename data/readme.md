**Ý nghĩa các file data**
1. atis.test.w-intent_origin.iob: raw test file chưa qua xử lý, format: BOS sentence EOS IOB_tagging intent, mỗi câu có thể có nhiều hơn một intent.
2. các file atis-2.dev.w-intent_origin.iob, atis-2.train.w-intent_origin.iob tương tự như trên.
3. intent_labels.txt chứa nhãn intent, sắp xếp theo thứ tự từ xuất hiện nhiều nhất đến ít nhất. 
4. slot_labels.txt chứa nhãn slot, sắp xếp theo thứ tự từ xuất hiện nhiều nhất đến ít nhất.
5. loc.csv, thang.csv, tu.csv, dat.csv là các file csv chứa ['En', 'VN', 'IOB', 'Intent'], tên của ai thì lấy về gán nhãn


**Các bước gán nhãn cho data**
1. lấy file csv về, chỉnh sửa các câu tiếng việt lại nếu cần
2. chuyển các file csv sau khi chỉnh sử câu tiếng việt hoàn chỉnh về dạng json bằng notebook convert_json.ipynb
3. dùng label studio gán nhãn
4. tải lên file completion.json vào thư mục này
