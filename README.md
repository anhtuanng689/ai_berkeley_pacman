# AI Berkeley Pacman

# Câu 1: DFS
- Đầu tiên, khởi tạo myStack bằng Stack lưu các node và mảng visitedNodes lưu vị trí, các bước di chuyển.
- Push trạng thái ban đầu vào myStack và thực hiện vòng lặp (Vòng lặp này sẽ lặp đến khi không còn phần tử nào trong myStack).
- Pop trạng thái đó ra và kiểm tra.
- Nếu trạng thái đó đã được xét thì bỏ qua vòng lặp, nếu không thì tiếp tục kiểm tra:
  + Nếu trạng thái đó là trạng thái đích, trả về các bước di chuyển và kết thúc.
  + Nếu không, lấy ra danh sách các successor của trạng thái đó, thêm danh sách di chuyển và chí phí của successor rồi push vào myStack.
# Câu 2: BFS
- Tương tự câu 1, thay đổi cấu trúc dữ liệu thành Queue.
# Câu 3: UCS
- Tương tự câu 1, thay đổi cấu trúc dữ liệu thành Priority Queue và tính thêm chi phí cost.
# Câu 4: A*
- Tương tự câu 3, chi phí cost ở đây được tính bằng hàm heuristic (Manhattan) + cost.
