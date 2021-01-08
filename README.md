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
# Câu 5: Finding All the Corners
- Tạo 1 mảng boolean để đánh dấu vị trị góc đã đi qua chưa với giá trị bằng False.
- Khi toàn bộ giá trị trong mảng là True thì dừng.
- Hàm getSuccessor trả về mảng gồm vị trí, các bước di chuyển và chi phí, trong đó state[0] là tọa độ, state[1] là mảng đánh dấu góc đã đi qua khi Pacman ở
state[0] và thực hiện các bước di chuyển.
- Kiểm tra Pacman có di chuyển 4 hướng được không, nếu được thì có di chuyển qua góc không, nếu có thì thay đổi mảng đánh dấu thành True rồi push vào successor.
# Câu 6: Corners Problem: Heuristic
- Heuristic được đánh giá bằng cách kiểm tra những góc chưa được thăm, nếu chưa được thăm thì heuristic sẽ là max của đường đi ngắn từ vị trí hiện tại của pacman đến các góc (đi theo từng ô và đi theo 4 hướng, giả sử không có vật cản).
# Câu 7: Eating All The Dots
- Heuristic là max của đường đi từ vị hiện tại của pacman đến các dots (đường đi từ vị trí hiên tại của pacman đến 1 dot được tính bằng hàm mazeDistance).
# Câu 8: Suboptimal Search
- Cài đặt hàm isGoalState của class AnyFoodSearchProblem, hàm findPathToClosestDot isGoalState kiểm tra xem vị trí hiện tại của pacman có trùng với vị trí của thức ăn không nếu có true, trả về false nếu ngược lại findPathToclosetDot dùng hàm ucs đã cài ở bài 3 trả về đường đi đến dot gần nhất.
