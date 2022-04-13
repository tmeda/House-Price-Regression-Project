<h1>The House Price Regression Project</h1>
    <h3>Introduction</h3>
        <p>Real estate is an exellent investment opportunity because of how versatile it is. From renting, to house flipping, to holding long term, real estate offers different strategies people can use to grow their money. No matter what strategy you use, the price that you purchase the house for determines how well your investment will perform. Over paying for an investment property can have detrimental effects that you may not be able to recover from. So how do we know when we are overpaying for an investment property? That is the goal of this project. <b>We want to use characteristics of a house to determine its value so that we have an idea of what we should be paying for it.</b></p>
    <h3>Repo Structure</h3>
        <p>For this project, I split my files into two main folders. In the data folder, I store the raw home price data along with a data dictionary. I also store the transformed data that the machine learning algorithms use in this folder. In the code folder, I store the code in notebooks that follow the steps taken for this project so that other people can understand my process. </p> 
    <h3>Sources</h3>
        <p>For this project, I collected data from the <a href='https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/overview'>Kaggle</a> platform.</p>
    <h3>The Data</h3>
        <p>The data used in this project has 1460 entries and 81 columns,38 numeric and 43 non-numeric. These columns describe different aspects of residential homes in Ames, Iowa.</p>
    <h3>Modeling</h3>
        <p>For this project, I developed 6 models. I developed 2 KNN regressors, 2 random forest regressors and one linear model. I also included the dummy regressor to serve as a baseline. I used the R^2,the coefficient of determination, to compare the models. This metric shows the percentage of the home sale price variation the model can explain. It can reach a maximum of 1 which indicates perfect prediction so we want the model that is as close to that limit as possible.</p>
        <h2>Model Performance</h2>
            <table style="width:100%;border:1px solid black;">
                <tr >
                    <th>Model</th>
                    <th>R^2</th>
                </tr>
                <tr>
                    <td>RandomForestRegressor(max_depth=64, random_state=0)</td>
                    <td>0.843</td>
                </tr>
                <tr>
                    <td>RandomForestRegressor(max_depth=16, random_state=0)</td>
                    <td>0.842</td>
                </tr>
                <tr>
                    <td>KNeighborsRegressor(n_neighbors=8)</td>
                    <td>0.687</td>
                </tr>
                <tr>
                    <td>KNeighborsRegressor(n_neighbors=2)</td>
                    <td>0.616</td>
                </tr>
                <tr>
                    <td>ElasticNet(random_state=0)</td>
                    <td>0.585</td>
                </tr>
                <tr>
                    <td>DummyRegressor()</td>
                    <td>0</td>
                </tr>
            </table>
    <h3>Conclusions</h3>
        <p>Looking at the performance of the models, both of the random forest models performed the best. Of these two models, I would use the second best option because it performs almost as well as the best model while using 1/4 of its computational resources. Considering that difference in the R^2 score is only 0.001, this tradeoff is worth it.</p>
    <h3>Next Steps</h3>
            <p>This project works well as a proof of concept for an even bigger application. This application could scrape websites such as Zillow.com for real estate data then learn from it to predict home prices. It would have more relevant data in larger quantities meaning it could perform better than the model developed in this project.</p>
