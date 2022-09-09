# Public research
CF Recommendation system using RFM Analysis and clustering techniques
## Cấu trúc file:

```
project
|___data
|   |   Data-The-New-Gym-sorted.xlsx
|   |   filtered_data.csv
|   |   rfm_data.csv
|   |   rfm_weight.csv
|
|___docs
|   |   Customer-Segmentation-Based-on-RFM-Model.pdf
|   |   FINAL-model.pdf
|   |   key-ref.pdf
|   |   ref-main.pdf
|
|___notebooks
|   |___cluster_first
|   |   |   clustering.ipynb
|   |   |   collaborative filtering.ipynb
|   |   |   train_test_split.ipynb
|   |   |   plot.ipynb
|   |   |   prepare_data.ipynb
|   |___split_first
|   |   |   clustering.ipynb
|   |   |   collaborative filtering.ipynb
|   |   |   plot.ipynb
|   |   |   prepare_data.ipynb
|   |   
|___processing_data.py
|   README.md
```

- `cluster_first`: Phân cụm trước rồi mới chia train test
- `split_first`: Chia train test rồi mới phân cụm

- `processing_data.py`: File này nhận một đường dẫn đến file excel và trả về file csv đã xử lý.
- `prepare_data.ipynb`: File này xử lý dữ liệu RFM từ file csv đã xử lý.
- `clustering.ipynb`: File này phân cụm dữ liệu từ dữ liệu RFM trên.
- `train_test_split.ipynb`: Chia train test sau khi phân cụm.
- `collaborative filtering.ipynb`: File này làm lọc cộng tác từ dữ liệu đã xử lý ở trên.

`prepare_data` -> `clustering` -> `train_test_split` -> `collaborative filtering`

## Test
- 80% train - 20% test
- Đưa data vào notebook, xong nó ra:
    - giá trị f1_score
    - Xuất ra những sản phẩm recommend
- So sánh với CF data gốc (rating là quantity x price)

### Temporary Note
không quan tâm chi nhánh
bỏ vế sau
membership - 2 tháng - 1
cust id, 
recency: thời gian cuối cùng mua (unit là week)
frequency: count transaction
price: sum all price
