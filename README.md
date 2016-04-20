# Test
# Simple C++ Code
#include <iostream>
#include <string>

void IntOrEquity(std::string iore);
void InsideInterval(double num);
void cumprod();
void numLetters(std::string word);


int main()
{
	IntOrEquity("INTEREST_RATE");
	IntOrEquity("EQUITY");
	IntOrEquity("REPO_RATE");
	std::cout << std::endl;
	
	InsideInterval(-2.5);
	InsideInterval(0.5);
	InsideInterval(2.5);
	std::cout << std::endl;

	cumprod();
	std::cout << std::endl;

	std::string comp = "computer";
	numLetters(comp);
	std::cout << std::endl;

	return 0;
}

void IntOrEquity(std::string iore)
{
	// Define a bool variable
	bool rate = true;
	bool equity = false;

	if (iore == "INTEREST_RATE")
	{
		std::cout << "Is it an interest rate? " << rate << std::endl;
	}
	else if (iore == "EQUITY")
	{
		rate = false;
		std::cout << "Is it an interest rate? " << equity << std::endl;
	}
	else
	{
		std::cout << "The type is not valid!" << std::endl;
	}
}

void InsideInterval(double num)
{
	if (num < -1.0)
	{
		std::cout << num << " is strictly less than -1.0" << std::endl;
	}
	else if (num >= -1.0 && num <= 1.0)
	{
		std::cout << num << " is in the interval [-1.0, 1.0]" << std::endl;
	}
	else
	{
		std::cout << num << " is strictly greater than 1.0" << std::endl;
	}
}

void cumprod()
{
	int prod = 1;

	// Calculate the cumulative product at each iteration
	for (int k = 1; k <= 10; ++k)
	{
		prod = prod * k;
		// Break out the loop when the cumulative product exceeds 250
		if (prod > 250)
		{
			std::cout << "Stop! The next product exceeds 250! " << std::endl;
			break;
		}
		std::cout << prod << ", ";
	}
}


void numLetters(std::string word)
{
	std::cout << "The number of characters in " << word << " is " << word.size() << std::endl;
}
