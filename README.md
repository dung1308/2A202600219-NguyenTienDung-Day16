# Lab 16

## 1. Idea reframed

**Original idea:**
> Xây dựng một AI Agent có khả năng chấm điểm bài văn và tư vấn học tập cho học sinh, giúp giảm tải công việc cho giáo viên Ngữ văn.

**Reframed as a product opportunity:**
> Hiện tại, giáo viên Ngữ văn đang bị quá tải bởi các công việc lặp đi lặp lại (chấm lỗi chính tả, dùng từ), dẫn đến việc phản hồi bài làm cho học sinh bị trễ (1-2 tuần). Chúng tôi nhận thấy cơ hội xây dựng một "Hệ điều hành chấm bài" dựa trên LLM, không chỉ lọc lỗi tự động mà còn cung cấp phản hồi tức thì (Instant Feedback). Niềm tin cốt lõi của chúng tôi là: Khi AI xử lý 80% lỗi cơ bản, con người có thể dành 100% tâm trí cho việc nuôi dưỡng cảm xúc và tư duy văn chương.

---

## 2. Customer / Segment Card

- **Segment name:** Giáo viên Ngữ văn cấp THCS tại khu vực ngoại thành và tỉnh thành đang chuyển đổi số giáo dục.
- **Operational context:** Phụ trách nhiều lớp với sĩ số đông (40–50 học sinh/lớp), vừa giảng dạy vừa kiêm nhiệm công tác chủ nhiệm, hồ sơ sổ sách và chấm bài định kỳ.
- **Recurring workflow:** Giao đề viết -> Thu bài giấy hoặc file online -> Đọc từng bài -> Sửa lỗi chính tả/ngữ pháp -> Nhận xét ngắn -> Chấm điểm theo barem -> Tổng hợp điểm báo cáo.
- **Pain moment:** Sau giờ dạy chính khóa vẫn phải mang cả chồng bài về nhà, dành buổi tối để chấm thủ công nhưng vẫn không kịp trả bài đúng hạn.
- **Why now:** Việc phổ cập thiết bị số trong trường học và AI tiếng Việt ngày càng tốt tạo cơ hội để giáo viên dùng trợ lý chấm bài mà không cần kỹ năng công nghệ cao.
- **Access path:** Tổ chuyên môn trong trường, phòng giáo dục địa phương, cộng đồng giáo viên trên Zalo / Facebook, các khóa tập huấn EdTech.

**One-sentence description:**
> Những giáo viên Ngữ văn tâm huyết nhưng bị quá tải, đang tìm kiếm công cụ để tự động hóa việc chấm điểm cơ bản nhằm tập trung vào giảng dạy chuyên sâu.

---

## 3. Need Map (2–3 needs)

### Need #1 (priority)
- **Statement (JTBD):** Khi chấm bài tập làm văn, tôi muốn AI tự động lọc và sửa các lỗi kỹ thuật (chính tả, cấu trúc), để tôi có thể dành thời gian đánh giá chiều sâu tư duy của học sinh.
- **Current workaround:** Chấm bài thủ công bằng bút đỏ vào ban đêm và cuối tuần.
- **Pain signal:** Sự mệt mỏi tinh thần; chất lượng nhận xét giảm dần đối với những bài ở cuối tập hồ sơ.
- **Evidence / proxy evidence:** Mất trung bình 20 giờ mỗi tuần chỉ để chấm bài; phản hồi bài viết thường đến tay học sinh khi các em đã quên nội dung mình viết.
- **Why underserved:** Các công cụ như Word hay Google Docs chỉ bắt được lỗi chính tả đơn thuần, không hiểu được mạch văn hay logic nghị luận.

### Need #2
- **Statement (JTBD):** Khi nhận lại bài chấm, học sinh muốn biết chính xác mình cần sửa câu văn nào ngay lúc đó, để kỹ năng viết được cải thiện tức thì.
- **Current workaround:** Chờ đợi giáo viên trả bài sau 1-2 tuần và nhận những lời phê chung chung như "Cần cố gắng thêm".
- **Pain signal:** Học sinh mất động lực viết; thường xuyên lặp lại lỗi sai cũ ở bài tiếp theo.
- **Evidence / proxy evidence:** Tỷ lệ học sinh đọc kỹ lời phê của giáo viên thấp (<20%) vì thời gian chờ đợi quá lâu.
- **Why underserved:** Giáo viên không có đủ thời gian để kèm cặp 1-1 cho từng học sinh về cách diễn đạt trong lúc các em đang viết.

---

## 4. Strategy Statement

For **giáo viên Ngữ văn cấp THCS tại khu vực ngoại thành và tỉnh thành**
who struggle with **áp lực chấm bài quá tải và phản hồi chậm**,
our product helps them **tăng tốc độ chấm bài lên 5 lần và cá nhân hóa phản hồi**
through **hệ thống AI Agent chấm điểm theo Rubric tùy chỉnh**,
unlike **việc chấm tay truyền thống hoặc các công cụ sửa lỗi chính tả đơn thuần**,
because we can leverage **khả năng phân tích ngữ cảnh và dữ liệu tiến bộ của học sinh theo thời gian**.

---

## 5. Moat Hypothesis

**Moat mechanism:** Domain-learning flywheel (Vòng quay học tập chuyên biệt).

If we deploy **[1,000]** times in **[chấm văn THPT tại Việt Nam]**, the following improve:
1. Độ chính xác của AI trong việc nhận diện các phong cách viết văn đặc thù của học sinh Việt Nam.
2. Thư viện nhận xét mẫu (Feedback Library) trở nên phong phú và "người" hơn.
3. Khả năng dự báo các lỗi phổ biến mà học sinh thường mắc phải theo từng chủ đề tác phẩm.

**Why competitors cannot easily replicate this:**
> Các đối thủ toàn cầu (như Grammarly) không hiểu sâu về chương trình giáo dục và cấu trúc thi cử Ngữ văn riêng biệt của Việt Nam. Dữ liệu tinh chỉnh (Fine-tuning) từ đội ngũ giáo viên bản địa chính là rào cản lớn nhất.

---

## 6. Initial TAM / SAM / SOM view

| Layer | Estimate | Key assumptions | Confidence |
|---|---|---|---|
| TAM | ~5US$18M – US$55M / năm (≈ 460 tỷ – 1.400 tỷ VND) | Fact-ish base: Việt Nam có hàng chục nghìn trường THCS/THPT và lực lượng giáo viên rất lớn. Assumption: phân khúc liên quan trực tiếp = giáo viên Ngữ văn THCS + THPT khoảng 70k–140k người. Assumption pricing: 180k–350k VND / giáo viên / tháng cho SaaS AI chấm bài. Công thức: Users × ARPU × 12 tháng. |  med - high |
| SAM | ~US$4.5M – US$16M / năm (≈ 115 tỷ – 410 tỷ VND) | Chỉ tính giáo viên Ngữ văn THCS tại khu vực ngoại thành + tỉnh thành, là segment đã chọn. Assumption: chiếm 25%–40% TAM users và chỉ 50%–70% có hạ tầng số + willingness-to-pay đủ dùng sản phẩm. | low-med |
| SOM | ~US$450k – US$2.4M ARR (≈ 11 tỷ – 61 tỷ VND) | chiếm 3%–15% SAM qua bottom-up GTM: pilot tỉnh/thành, referral giáo viên, bán qua trường/LMS. Tương đương khoảng 2k–10k giáo viên trả phí ở mức 180k–350k/tháng. | low |

**Top 3 unknowns requiring further research:**
1. Khả năng đọc chữ viết tay (OCR) thực tế đối với bài thi giấy.
2. Mức độ chấp nhận của Bộ Giáo dục đối với việc đưa AI vào quy trình chấm điểm chính thức.
3. Chi phí vận hành API (Token cost) khi xử lý các bài văn dài.

**Judgment:**
- [x] Worth pursuing now

---

## 7. Positioning Note (2 sentences)

**What we are:**
> Một trợ lý AI chuyên sâu giúp giáo viên Ngữ văn tự động hóa việc chấm điểm và quản lý lộ trình kỹ năng viết của học sinh.

**What we are not / not yet:**
> Một công cụ viết văn hộ (Ghostwriter) hay một hệ thống thay thế hoàn toàn vai trò thẩm định nghệ thuật của giáo viên.

---

## 8. Self-assessment before Day 17

Trong 6 mắt xích, mắt xích chúng tôi tự tin nhất là **Need (Nhu cầu)** vì nỗi đau của giáo viên Văn là rất thực tế. Mắt xích yếu nhất là **Moat (Rào cản)** vì cần một lượng dữ liệu lớn ban đầu để AI chấm "mượt" như người.

**Open questions chúng tôi muốn khám phá thêm ở Day 17:**
1. Làm sao để thiết kế UX giúp giáo viên tin tưởng vào kết quả chấm của AI?
2. Quy trình "Human-in-the-loop" (người kiểm soát) nên đặt ở bước nào là hiệu quả nhất?
3. Mô hình kinh doanh nào phù hợp (B2B bán cho trường hay B2C bán cho học sinh)?

