# Retail-Sales-Analysis
I am doing a practical analysis of Sales for a Retail Shop. 
# Creating the dataset
sales_data <- data.frame(
  Month = c("January", "January", "February", "February", "March", "March"),
  Product = c("Product A", "Product B", "Product A", "Product B", "Product A", "Product B"),
  Units_Sold = c(120, 80, 150, 95, 130, 110),
  Unit_Price = c(500, 300, 500, 300, 500, 300),
  Revenue = c(60000, 24000, 75000, 28500, 65000, 33000),
  Expenses = c(25000, 10000, 30000, 12000, 27000, 15000),
  Profit = c(35000, 14000, 45000, 16500, 38000, 18000)
)

# View the data
print(sales_data)
# Calculate total revenue
total_revenue <- sum(sales_data$Revenue)

# Calculate total expenses
total_expenses <- sum(sales_data$Expenses)

# Calculate total profit
total_profit <- sum(sales_data$Profit)

# Print the results
cat("Total Revenue for Q1:", total_revenue, "\n")
cat("Total Expenses for Q1:", total_expenses, "\n")
cat("Total Profit for Q1:", total_profit, "\n")
# Install ggplot2 if you haven't already
install.packages("ggplot2")

# Load the ggplot2 library
library(ggplot2)

# Create a line plot showing revenue over the months
ggplot(sales_data, aes(x = Month, y = Revenue, group = Product, color = Product)) +
  geom_line(size = 1) +
  geom_point() +
  labs(title = "Revenue by Product Over the First Quarter",
       x = "Month", y = "Revenue (KSh)") +
  theme_minimal()
