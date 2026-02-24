{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "code",
      "execution_count": null,
      "metadata": {
        "id": "btQe0Quj-erm"
      },
      "outputs": [],
      "source": [
        "import pandas as pd\n",
        "\n",
        "df = pd.read_csv(\"HRDataset_v14.csv\")\n",
        "\n",
        "# Attrition Flag\n",
        "df['Attrition'] = df['EmploymentStatus'].apply(\n",
        "    lambda x: 1 if x != 'Active' else 0\n",
        ")\n",
        "\n",
        "# Save cleaned file\n",
        "df.to_csv(\"HR_Cleaned.csv\", index=False)"
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df.shape"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "F8xoEZo2AM_b",
        "outputId": "15bdfcbd-0d30-4118-caf9-1317d0ce082c"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "(311, 37)"
            ]
          },
          "metadata": {},
          "execution_count": 3
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df.columns"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "U-b0jX-hASjz",
        "outputId": "721e7c4f-470a-4828-a7da-3d591fef5a1f"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Index(['Employee_Name', 'EmpID', 'MarriedID', 'MaritalStatusID', 'GenderID',\n",
              "       'EmpStatusID', 'DeptID', 'PerfScoreID', 'FromDiversityJobFairID',\n",
              "       'Salary', 'Termd', 'PositionID', 'Position', 'State', 'Zip', 'DOB',\n",
              "       'Sex', 'MaritalDesc', 'CitizenDesc', 'HispanicLatino', 'RaceDesc',\n",
              "       'DateofHire', 'DateofTermination', 'TermReason', 'EmploymentStatus',\n",
              "       'Department', 'ManagerName', 'ManagerID', 'RecruitmentSource',\n",
              "       'PerformanceScore', 'EngagementSurvey', 'EmpSatisfaction',\n",
              "       'SpecialProjectsCount', 'LastPerformanceReview_Date', 'DaysLateLast30',\n",
              "       'Absences', 'Attrition'],\n",
              "      dtype='object')"
            ]
          },
          "metadata": {},
          "execution_count": 4
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df.head()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 325
        },
        "id": "Yz4PVDUuAVhJ",
        "outputId": "c934a57e-4fc6-45a3-fe21-914a8bb96922"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "              Employee_Name  EmpID  MarriedID  MaritalStatusID  GenderID  \\\n",
              "0       Adinolfi, Wilson  K  10026          0                0         1   \n",
              "1  Ait Sidi, Karthikeyan     10084          1                1         1   \n",
              "2         Akinkuolie, Sarah  10196          1                1         0   \n",
              "3              Alagbe,Trina  10088          1                1         0   \n",
              "4          Anderson, Carol   10069          0                2         0   \n",
              "\n",
              "   EmpStatusID  DeptID  PerfScoreID  FromDiversityJobFairID  Salary  ...  \\\n",
              "0            1       5            4                       0   62506  ...   \n",
              "1            5       3            3                       0  104437  ...   \n",
              "2            5       5            3                       0   64955  ...   \n",
              "3            1       5            3                       0   64991  ...   \n",
              "4            5       5            3                       0   50825  ...   \n",
              "\n",
              "   ManagerID  RecruitmentSource PerformanceScore EngagementSurvey  \\\n",
              "0       22.0           LinkedIn          Exceeds             4.60   \n",
              "1        4.0             Indeed      Fully Meets             4.96   \n",
              "2       20.0           LinkedIn      Fully Meets             3.02   \n",
              "3       16.0             Indeed      Fully Meets             4.84   \n",
              "4       39.0      Google Search      Fully Meets             5.00   \n",
              "\n",
              "   EmpSatisfaction SpecialProjectsCount LastPerformanceReview_Date  \\\n",
              "0                5                    0                  1/17/2019   \n",
              "1                3                    6                  2/24/2016   \n",
              "2                3                    0                  5/15/2012   \n",
              "3                5                    0                   1/3/2019   \n",
              "4                4                    0                   2/1/2016   \n",
              "\n",
              "  DaysLateLast30 Absences Attrition  \n",
              "0              0        1         0  \n",
              "1              0       17         1  \n",
              "2              0        3         1  \n",
              "3              0       15         0  \n",
              "4              0        2         1  \n",
              "\n",
              "[5 rows x 37 columns]"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-12ef59cc-a1f7-4509-a742-07a2901e027a\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Employee_Name</th>\n",
              "      <th>EmpID</th>\n",
              "      <th>MarriedID</th>\n",
              "      <th>MaritalStatusID</th>\n",
              "      <th>GenderID</th>\n",
              "      <th>EmpStatusID</th>\n",
              "      <th>DeptID</th>\n",
              "      <th>PerfScoreID</th>\n",
              "      <th>FromDiversityJobFairID</th>\n",
              "      <th>Salary</th>\n",
              "      <th>...</th>\n",
              "      <th>ManagerID</th>\n",
              "      <th>RecruitmentSource</th>\n",
              "      <th>PerformanceScore</th>\n",
              "      <th>EngagementSurvey</th>\n",
              "      <th>EmpSatisfaction</th>\n",
              "      <th>SpecialProjectsCount</th>\n",
              "      <th>LastPerformanceReview_Date</th>\n",
              "      <th>DaysLateLast30</th>\n",
              "      <th>Absences</th>\n",
              "      <th>Attrition</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Adinolfi, Wilson  K</td>\n",
              "      <td>10026</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>4</td>\n",
              "      <td>0</td>\n",
              "      <td>62506</td>\n",
              "      <td>...</td>\n",
              "      <td>22.0</td>\n",
              "      <td>LinkedIn</td>\n",
              "      <td>Exceeds</td>\n",
              "      <td>4.60</td>\n",
              "      <td>5</td>\n",
              "      <td>0</td>\n",
              "      <td>1/17/2019</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>Ait Sidi, Karthikeyan</td>\n",
              "      <td>10084</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>104437</td>\n",
              "      <td>...</td>\n",
              "      <td>4.0</td>\n",
              "      <td>Indeed</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>4.96</td>\n",
              "      <td>3</td>\n",
              "      <td>6</td>\n",
              "      <td>2/24/2016</td>\n",
              "      <td>0</td>\n",
              "      <td>17</td>\n",
              "      <td>1</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Akinkuolie, Sarah</td>\n",
              "      <td>10196</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>5</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>64955</td>\n",
              "      <td>...</td>\n",
              "      <td>20.0</td>\n",
              "      <td>LinkedIn</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>3.02</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>5/15/2012</td>\n",
              "      <td>0</td>\n",
              "      <td>3</td>\n",
              "      <td>1</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Alagbe,Trina</td>\n",
              "      <td>10088</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>64991</td>\n",
              "      <td>...</td>\n",
              "      <td>16.0</td>\n",
              "      <td>Indeed</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>4.84</td>\n",
              "      <td>5</td>\n",
              "      <td>0</td>\n",
              "      <td>1/3/2019</td>\n",
              "      <td>0</td>\n",
              "      <td>15</td>\n",
              "      <td>0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Anderson, Carol</td>\n",
              "      <td>10069</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>0</td>\n",
              "      <td>5</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>50825</td>\n",
              "      <td>...</td>\n",
              "      <td>39.0</td>\n",
              "      <td>Google Search</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>5.00</td>\n",
              "      <td>4</td>\n",
              "      <td>0</td>\n",
              "      <td>2/1/2016</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>1</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "<p>5 rows × 37 columns</p>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-12ef59cc-a1f7-4509-a742-07a2901e027a')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-12ef59cc-a1f7-4509-a742-07a2901e027a button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-12ef59cc-a1f7-4509-a742-07a2901e027a');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "variable_name": "df"
            }
          },
          "metadata": {},
          "execution_count": 5
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# core HR KPI\n",
        "# Total Employees\n",
        "total_employees = df.shape[0]\n",
        "\n",
        "# Active Employees\n",
        "active_employees = df[df['EmploymentStatus'] == 'Active'].shape[0]\n",
        "\n",
        "# Attrition Count\n",
        "attrition_count = df[df['Attrition'] == 1].shape[0]\n",
        "\n",
        "# Attrition Rate %\n",
        "attrition_rate = round((attrition_count / total_employees) * 100, 2)\n",
        "\n",
        "# Average Salary\n",
        "avg_salary = round(df['Salary'].mean(), 2)\n",
        "\n",
        "total_employees, active_employees, attrition_count, attrition_rate, avg_salary"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "iK8E22LNA1uE",
        "outputId": "d36015c8-25e3-417d-b287-13abf2e84b40"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "(311, 207, 104, 33.44, np.float64(69020.68))"
            ]
          },
          "metadata": {},
          "execution_count": 6
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "dept_attrition = df.groupby('Department')['Attrition'].mean().sort_values(ascending=False) * 100\n",
        "dept_attrition"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 303
        },
        "id": "UlnBpxPEBBVI",
        "outputId": "cda01239-3234-4b3f-9b03-b454a67cdbdb"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Department\n",
              "Production              39.712919\n",
              "Software Engineering    36.363636\n",
              "Admin Offices           22.222222\n",
              "IT/IS                   20.000000\n",
              "Sales                   16.129032\n",
              "Executive Office         0.000000\n",
              "Name: Attrition, dtype: float64"
            ],
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Attrition</th>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Department</th>\n",
              "      <th></th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>Production</th>\n",
              "      <td>39.712919</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Software Engineering</th>\n",
              "      <td>36.363636</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Admin Offices</th>\n",
              "      <td>22.222222</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>IT/IS</th>\n",
              "      <td>20.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Sales</th>\n",
              "      <td>16.129032</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Executive Office</th>\n",
              "      <td>0.000000</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div><br><label><b>dtype:</b> float64</label>"
            ]
          },
          "metadata": {},
          "execution_count": 7
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "gender_dist = df['Sex'].value_counts()\n",
        "gender_dist"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 178
        },
        "id": "QzaJQcY9BSoY",
        "outputId": "df5a4b7a-0efa-4f2d-afc7-10bd18852bf0"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "Sex\n",
              "F     176\n",
              "M     135\n",
              "Name: count, dtype: int64"
            ],
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>count</th>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>Sex</th>\n",
              "      <th></th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>F</th>\n",
              "      <td>176</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>M</th>\n",
              "      <td>135</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div><br><label><b>dtype:</b> int64</label>"
            ]
          },
          "metadata": {},
          "execution_count": 8
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df['DOB'] = pd.to_datetime(df['DOB'], errors='coerce')\n",
        "\n",
        "# Calculate Age\n",
        "today = pd.to_datetime(\"today\")\n",
        "df['Age'] = (today - df['DOB']).dt.days // 365\n",
        "\n",
        "# Check result\n",
        "df[['DOB', 'Age']].head()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 261
        },
        "id": "odaK7tTaB_zf",
        "outputId": "b6a86b5d-97bd-4618-ad06-daa1a49d494d"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stderr",
          "text": [
            "/tmp/ipython-input-1381739067.py:1: UserWarning: Could not infer format, so each element will be parsed individually, falling back to `dateutil`. To ensure parsing is consistent and as-expected, please specify a format.\n",
            "  df['DOB'] = pd.to_datetime(df['DOB'], errors='coerce')\n"
          ]
        },
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "         DOB  Age\n",
              "0 1983-07-10   42\n",
              "1 2075-05-05  -50\n",
              "2 1988-09-19   37\n",
              "3 1988-09-27   37\n",
              "4 1989-09-08   36"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-c8724a4d-412d-4363-83e9-063b89fce448\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>DOB</th>\n",
              "      <th>Age</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>1983-07-10</td>\n",
              "      <td>42</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>2075-05-05</td>\n",
              "      <td>-50</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>1988-09-19</td>\n",
              "      <td>37</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>1988-09-27</td>\n",
              "      <td>37</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>1989-09-08</td>\n",
              "      <td>36</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-c8724a4d-412d-4363-83e9-063b89fce448')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-c8724a4d-412d-4363-83e9-063b89fce448 button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-c8724a4d-412d-4363-83e9-063b89fce448');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "summary": "{\n  \"name\": \"df[['DOB', 'Age']]\",\n  \"rows\": 5,\n  \"fields\": [\n    {\n      \"column\": \"DOB\",\n      \"properties\": {\n        \"dtype\": \"date\",\n        \"min\": \"1983-07-10 00:00:00\",\n        \"max\": \"2075-05-05 00:00:00\",\n        \"num_unique_values\": 5,\n        \"samples\": [\n          \"2075-05-05 00:00:00\",\n          \"1989-09-08 00:00:00\",\n          \"1988-09-19 00:00:00\"\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    },\n    {\n      \"column\": \"Age\",\n      \"properties\": {\n        \"dtype\": \"number\",\n        \"std\": 39,\n        \"min\": -50,\n        \"max\": 42,\n        \"num_unique_values\": 4,\n        \"samples\": [\n          -50,\n          36,\n          42\n        ],\n        \"semantic_type\": \"\",\n        \"description\": \"\"\n      }\n    }\n  ]\n}"
            }
          },
          "metadata": {},
          "execution_count": 10
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df['Age'].describe()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 335
        },
        "id": "Fs_trmEkCHiE",
        "outputId": "bffbdf69-9961-45fd-a601-70b3a27b7305"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "count    311.000000\n",
              "mean      14.279743\n",
              "std       39.772201\n",
              "min      -50.000000\n",
              "25%      -39.500000\n",
              "50%       38.000000\n",
              "75%       42.500000\n",
              "max       50.000000\n",
              "Name: Age, dtype: float64"
            ],
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Age</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>count</th>\n",
              "      <td>311.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>mean</th>\n",
              "      <td>14.279743</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>std</th>\n",
              "      <td>39.772201</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>min</th>\n",
              "      <td>-50.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>25%</th>\n",
              "      <td>-39.500000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>50%</th>\n",
              "      <td>38.000000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>75%</th>\n",
              "      <td>42.500000</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>max</th>\n",
              "      <td>50.000000</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div><br><label><b>dtype:</b> float64</label>"
            ]
          },
          "metadata": {},
          "execution_count": 11
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "bins = [18,25,35,45,55,65]\n",
        "labels = ['18-25','26-35','36-45','46-55','56-65']\n",
        "\n",
        "df['AgeGroup'] = pd.cut(df['Age'], bins=bins, labels=labels)\n",
        "df['AgeGroup'].value_counts()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 272
        },
        "id": "RQIfz4eVCSX_",
        "outputId": "e789abfd-0fb1-4bfb-cfc4-41974e5e5ceb"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "AgeGroup\n",
              "36-45    153\n",
              "46-55     47\n",
              "26-35     11\n",
              "18-25      0\n",
              "56-65      0\n",
              "Name: count, dtype: int64"
            ],
            "text/html": [
              "<div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>count</th>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>AgeGroup</th>\n",
              "      <th></th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>36-45</th>\n",
              "      <td>153</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>46-55</th>\n",
              "      <td>47</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>26-35</th>\n",
              "      <td>11</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>18-25</th>\n",
              "      <td>0</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>56-65</th>\n",
              "      <td>0</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "</div><br><label><b>dtype:</b> int64</label>"
            ]
          },
          "metadata": {},
          "execution_count": 12
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "df.to_csv(\"HR_Cleaned_Final.csv\", index=False)"
      ],
      "metadata": {
        "id": "6PZb5B3pCVPJ"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "import pandas as pd\n",
        "import numpy as np\n",
        "import matplotlib.pyplot as plt\n",
        "import seaborn as sns\n",
        "\n",
        "# Load dataset\n",
        "df = pd.read_csv(\"HR_Cleaned_Final.csv\")\n",
        "\n",
        "# Quick check\n",
        "df.head()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 325
        },
        "id": "j9BhaFFiDwo2",
        "outputId": "13aff05e-0ff4-46a3-fd95-d91f5cf1a287"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "execute_result",
          "data": {
            "text/plain": [
              "              Employee_Name  EmpID  MarriedID  MaritalStatusID  GenderID  \\\n",
              "0       Adinolfi, Wilson  K  10026          0                0         1   \n",
              "1  Ait Sidi, Karthikeyan     10084          1                1         1   \n",
              "2         Akinkuolie, Sarah  10196          1                1         0   \n",
              "3              Alagbe,Trina  10088          1                1         0   \n",
              "4          Anderson, Carol   10069          0                2         0   \n",
              "\n",
              "   EmpStatusID  DeptID  PerfScoreID  FromDiversityJobFairID  Salary  ...  \\\n",
              "0            1       5            4                       0   62506  ...   \n",
              "1            5       3            3                       0  104437  ...   \n",
              "2            5       5            3                       0   64955  ...   \n",
              "3            1       5            3                       0   64991  ...   \n",
              "4            5       5            3                       0   50825  ...   \n",
              "\n",
              "   PerformanceScore  EngagementSurvey EmpSatisfaction SpecialProjectsCount  \\\n",
              "0           Exceeds              4.60               5                    0   \n",
              "1       Fully Meets              4.96               3                    6   \n",
              "2       Fully Meets              3.02               3                    0   \n",
              "3       Fully Meets              4.84               5                    0   \n",
              "4       Fully Meets              5.00               4                    0   \n",
              "\n",
              "   LastPerformanceReview_Date DaysLateLast30 Absences Attrition Age AgeGroup  \n",
              "0                   1/17/2019              0        1         0  42    36-45  \n",
              "1                   2/24/2016              0       17         1 -50      NaN  \n",
              "2                   5/15/2012              0        3         1  37    36-45  \n",
              "3                    1/3/2019              0       15         0  37    36-45  \n",
              "4                    2/1/2016              0        2         1  36    36-45  \n",
              "\n",
              "[5 rows x 39 columns]"
            ],
            "text/html": [
              "\n",
              "  <div id=\"df-ef8e38f5-4acb-408e-836f-2cd66304d835\" class=\"colab-df-container\">\n",
              "    <div>\n",
              "<style scoped>\n",
              "    .dataframe tbody tr th:only-of-type {\n",
              "        vertical-align: middle;\n",
              "    }\n",
              "\n",
              "    .dataframe tbody tr th {\n",
              "        vertical-align: top;\n",
              "    }\n",
              "\n",
              "    .dataframe thead th {\n",
              "        text-align: right;\n",
              "    }\n",
              "</style>\n",
              "<table border=\"1\" class=\"dataframe\">\n",
              "  <thead>\n",
              "    <tr style=\"text-align: right;\">\n",
              "      <th></th>\n",
              "      <th>Employee_Name</th>\n",
              "      <th>EmpID</th>\n",
              "      <th>MarriedID</th>\n",
              "      <th>MaritalStatusID</th>\n",
              "      <th>GenderID</th>\n",
              "      <th>EmpStatusID</th>\n",
              "      <th>DeptID</th>\n",
              "      <th>PerfScoreID</th>\n",
              "      <th>FromDiversityJobFairID</th>\n",
              "      <th>Salary</th>\n",
              "      <th>...</th>\n",
              "      <th>PerformanceScore</th>\n",
              "      <th>EngagementSurvey</th>\n",
              "      <th>EmpSatisfaction</th>\n",
              "      <th>SpecialProjectsCount</th>\n",
              "      <th>LastPerformanceReview_Date</th>\n",
              "      <th>DaysLateLast30</th>\n",
              "      <th>Absences</th>\n",
              "      <th>Attrition</th>\n",
              "      <th>Age</th>\n",
              "      <th>AgeGroup</th>\n",
              "    </tr>\n",
              "  </thead>\n",
              "  <tbody>\n",
              "    <tr>\n",
              "      <th>0</th>\n",
              "      <td>Adinolfi, Wilson  K</td>\n",
              "      <td>10026</td>\n",
              "      <td>0</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>4</td>\n",
              "      <td>0</td>\n",
              "      <td>62506</td>\n",
              "      <td>...</td>\n",
              "      <td>Exceeds</td>\n",
              "      <td>4.60</td>\n",
              "      <td>5</td>\n",
              "      <td>0</td>\n",
              "      <td>1/17/2019</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>42</td>\n",
              "      <td>36-45</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>1</th>\n",
              "      <td>Ait Sidi, Karthikeyan</td>\n",
              "      <td>10084</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>104437</td>\n",
              "      <td>...</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>4.96</td>\n",
              "      <td>3</td>\n",
              "      <td>6</td>\n",
              "      <td>2/24/2016</td>\n",
              "      <td>0</td>\n",
              "      <td>17</td>\n",
              "      <td>1</td>\n",
              "      <td>-50</td>\n",
              "      <td>NaN</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>2</th>\n",
              "      <td>Akinkuolie, Sarah</td>\n",
              "      <td>10196</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>5</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>64955</td>\n",
              "      <td>...</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>3.02</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>5/15/2012</td>\n",
              "      <td>0</td>\n",
              "      <td>3</td>\n",
              "      <td>1</td>\n",
              "      <td>37</td>\n",
              "      <td>36-45</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>3</th>\n",
              "      <td>Alagbe,Trina</td>\n",
              "      <td>10088</td>\n",
              "      <td>1</td>\n",
              "      <td>1</td>\n",
              "      <td>0</td>\n",
              "      <td>1</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>64991</td>\n",
              "      <td>...</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>4.84</td>\n",
              "      <td>5</td>\n",
              "      <td>0</td>\n",
              "      <td>1/3/2019</td>\n",
              "      <td>0</td>\n",
              "      <td>15</td>\n",
              "      <td>0</td>\n",
              "      <td>37</td>\n",
              "      <td>36-45</td>\n",
              "    </tr>\n",
              "    <tr>\n",
              "      <th>4</th>\n",
              "      <td>Anderson, Carol</td>\n",
              "      <td>10069</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>0</td>\n",
              "      <td>5</td>\n",
              "      <td>5</td>\n",
              "      <td>3</td>\n",
              "      <td>0</td>\n",
              "      <td>50825</td>\n",
              "      <td>...</td>\n",
              "      <td>Fully Meets</td>\n",
              "      <td>5.00</td>\n",
              "      <td>4</td>\n",
              "      <td>0</td>\n",
              "      <td>2/1/2016</td>\n",
              "      <td>0</td>\n",
              "      <td>2</td>\n",
              "      <td>1</td>\n",
              "      <td>36</td>\n",
              "      <td>36-45</td>\n",
              "    </tr>\n",
              "  </tbody>\n",
              "</table>\n",
              "<p>5 rows × 39 columns</p>\n",
              "</div>\n",
              "    <div class=\"colab-df-buttons\">\n",
              "\n",
              "  <div class=\"colab-df-container\">\n",
              "    <button class=\"colab-df-convert\" onclick=\"convertToInteractive('df-ef8e38f5-4acb-408e-836f-2cd66304d835')\"\n",
              "            title=\"Convert this dataframe to an interactive table.\"\n",
              "            style=\"display:none;\">\n",
              "\n",
              "  <svg xmlns=\"http://www.w3.org/2000/svg\" height=\"24px\" viewBox=\"0 -960 960 960\">\n",
              "    <path d=\"M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z\"/>\n",
              "  </svg>\n",
              "    </button>\n",
              "\n",
              "  <style>\n",
              "    .colab-df-container {\n",
              "      display:flex;\n",
              "      gap: 12px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert {\n",
              "      background-color: #E8F0FE;\n",
              "      border: none;\n",
              "      border-radius: 50%;\n",
              "      cursor: pointer;\n",
              "      display: none;\n",
              "      fill: #1967D2;\n",
              "      height: 32px;\n",
              "      padding: 0 0 0 0;\n",
              "      width: 32px;\n",
              "    }\n",
              "\n",
              "    .colab-df-convert:hover {\n",
              "      background-color: #E2EBFA;\n",
              "      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);\n",
              "      fill: #174EA6;\n",
              "    }\n",
              "\n",
              "    .colab-df-buttons div {\n",
              "      margin-bottom: 4px;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert {\n",
              "      background-color: #3B4455;\n",
              "      fill: #D2E3FC;\n",
              "    }\n",
              "\n",
              "    [theme=dark] .colab-df-convert:hover {\n",
              "      background-color: #434B5C;\n",
              "      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);\n",
              "      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));\n",
              "      fill: #FFFFFF;\n",
              "    }\n",
              "  </style>\n",
              "\n",
              "    <script>\n",
              "      const buttonEl =\n",
              "        document.querySelector('#df-ef8e38f5-4acb-408e-836f-2cd66304d835 button.colab-df-convert');\n",
              "      buttonEl.style.display =\n",
              "        google.colab.kernel.accessAllowed ? 'block' : 'none';\n",
              "\n",
              "      async function convertToInteractive(key) {\n",
              "        const element = document.querySelector('#df-ef8e38f5-4acb-408e-836f-2cd66304d835');\n",
              "        const dataTable =\n",
              "          await google.colab.kernel.invokeFunction('convertToInteractive',\n",
              "                                                    [key], {});\n",
              "        if (!dataTable) return;\n",
              "\n",
              "        const docLinkHtml = 'Like what you see? Visit the ' +\n",
              "          '<a target=\"_blank\" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'\n",
              "          + ' to learn more about interactive tables.';\n",
              "        element.innerHTML = '';\n",
              "        dataTable['output_type'] = 'display_data';\n",
              "        await google.colab.output.renderOutput(dataTable, element);\n",
              "        const docLink = document.createElement('div');\n",
              "        docLink.innerHTML = docLinkHtml;\n",
              "        element.appendChild(docLink);\n",
              "      }\n",
              "    </script>\n",
              "  </div>\n",
              "\n",
              "\n",
              "    </div>\n",
              "  </div>\n"
            ],
            "application/vnd.google.colaboratory.intrinsic+json": {
              "type": "dataframe",
              "variable_name": "df"
            }
          },
          "metadata": {},
          "execution_count": 14
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "#HR KPIs Calculation\n",
        "\n",
        "total_employees = df.shape[0]\n",
        "attrition_count = df['Attrition'].sum()\n",
        "attrition_rate = round((attrition_count / total_employees) * 100, 2)\n",
        "\n",
        "avg_salary = round(df['Salary'].mean(), 2)\n",
        "avg_engagement = round(df['EngagementSurvey'].mean(), 2)\n",
        "avg_satisfaction = round(df['EmpSatisfaction'].mean(), 2)\n",
        "avg_absence = round(df['Absences'].mean(), 2)\n",
        "\n",
        "print(\"Total Employees:\", total_employees)\n",
        "print(\"Attrition Count:\", attrition_count)\n",
        "print(\"Attrition Rate %:\", attrition_rate)\n",
        "print(\"Average Salary:\", avg_salary)\n",
        "print(\"Avg Engagement Score:\", avg_engagement)\n",
        "print(\"Avg Satisfaction:\", avg_satisfaction)\n",
        "print(\"Avg Absences:\", avg_absence)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "wMa12hyAD80P",
        "outputId": "1e609a47-98e9-49d8-9301-388ed134bce6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Total Employees: 311\n",
            "Attrition Count: 104\n",
            "Attrition Rate %: 33.44\n",
            "Average Salary: 69020.68\n",
            "Avg Engagement Score: 4.11\n",
            "Avg Satisfaction: 3.89\n",
            "Avg Absences: 10.24\n"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(8,5))\n",
        "sns.countplot(data=df, x='Department', hue='Attrition')\n",
        "plt.xticks(rotation=45)\n",
        "plt.title(\"Attrition by Department\")\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 588
        },
        "id": "mn0zCAgFEKg7",
        "outputId": "bda540c7-eca2-4acd-e898-7cd3d3c272f4"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 800x500 with 1 Axes>"
            ],
            "image/png": "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ERERfQyGWyIiIiLSDIZbIiIiItIMhlsiIiIi0gyGWyIiIiLSDIZbIiIiItIMhlsiIiIi0gyGWyIiIiLSDIZbIiIiItIMnqGMiIiIKB149EvxVL2+nCOvpur1pRT23BIRERHRJzty5Ajq1asHV1dX6HQ6bNmyRZU6GG6JiIiI6JNFR0ejZMmSmDt3rqp1cFgCEREREX2yWrVqoVatWmqXwZ5bIiIiItIOhlsiIiIi0gyGWyIiIiLSDIZbIiIiItIMhlsiIiIi0gzOlkBEREREnywqKgp3795Vlv39/XHp0iU4ODggZ86cqVYHwy0RERFROpDWzxh27tw5eHp6Kst9+/YFALRr1w7Lli1LtToYbomIiIjok1WtWhUionYZHHNLRERERNrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtERESkMr1er3YJaUJK3A+cLYGIiIhIJRYWFjAxMUFAQAAcHR1hYWEBnU6ndlmpTkQQFxeHZ8+ewcTEBBYWFsneF8MtERERkUpMTEyQJ08eBAYGIiAgQO1yVJchQwbkzJkTJibJH1zAcEtERESkIgsLC+TMmRMJCQlITExUuxzVmJqawszM7JN7rhluiYiIiFSm0+lgbm4Oc3NztUtJ93hAGRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWmGquH2yJEjqFevHlxdXaHT6bBlyxaj9SKCkSNHIlu2bLC2tkb16tVx584do21CQ0PRqlUr2Nrawt7eHp06dUJUVFQq3goiIiIiSitUDbfR0dEoWbIk5s6d+871kydPxqxZszB//nycPn0aGTNmRI0aNfD69Wtlm1atWuH69evYv38/duzYgSNHjuDHH39MrZtARERERGmImZpXXqtWLdSqVeud60QEM2bMwPDhw1G/fn0AwPLly+Hs7IwtW7agRYsWuHHjBvbs2YOzZ8+ibNmyAIDZs2ejdu3amDp1KlxdXd+579jYWMTGxirLERERKXzLiIiIiEgNaXbMrb+/P4KCglC9enWlzc7ODh4eHjh58iQA4OTJk7C3t1eCLQBUr14dJiYmOH369Hv3PXHiRNjZ2Sl/bm5un++GEBEREVGqSbPhNigoCADg7Oxs1O7s7KysCwoKgpOTk9F6MzMzODg4KNu8y5AhQxAeHq78PX78OIWrJyIiIiI1qDosQS2WlpawtLRUuwwiIiIiSmFptufWxcUFABAcHGzUHhwcrKxzcXFBSEiI0fqEhASEhoYq2xARERHRlyPNhts8efLAxcUFBw4cUNoiIiJw+vRpVKhQAQBQoUIFhIWF4fz588o2Bw8ehF6vh4eHR6rXTERERETqUnVYQlRUFO7evass+/v749KlS3BwcEDOnDnRu3dvjBs3DgUKFECePHkwYsQIuLq6okGDBgCAIkWKoGbNmujSpQvmz5+P+Ph4+Pj4oEWLFu+dKYGIiIiItEvVcHvu3Dl4enoqy3379gUAtGvXDsuWLcPAgQMRHR2NH3/8EWFhYahcuTL27NkDKysr5TKrVq2Cj48PqlWrBhMTEzRu3BizZs1K9dtCREREROrTiYioXYTaIiIiYGdnh/DwcNja2v7rtu4DlqdSVcl3fkpbtUsgIiIiSlEfmtfS7JhbIiIiIqKPxXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmsFwS0RERESawXBLRERERJrBcEtEREREmmGmdgGU8h79UlztEj5IzpFX1S6BiIiINIY9t0RERESkGQy3RERERKQZDLdEREREpBkMt0RERESkGWk63CYmJmLEiBHIkycPrK2tkS9fPowdOxYiomwjIhg5ciSyZcsGa2trVK9eHXfu3FGxaiIiIiJSS5oOt5MmTcK8efMwZ84c3LhxA5MmTcLkyZMxe/ZsZZvJkydj1qxZmD9/Pk6fPo2M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3NywdOlSpS1PnjzK/0UEM2bMwPDhw1G/fn0AwPLly+Hs7IwtW7agRYsWKVYLEREREaV9yeq5dXNzw/Hjx5O0Hz9+HK6urp9clMG2bdtQtmxZNG3aFE5OTihdujQWLVqkrPf390dQUBCqV6+utNnZ2cHDwwMnT558735jY2MRERFh9EdERERE6V+ywm2XLl3Qu3dvLF26FA8fPsTDhw+xZMkS9OnTJ8k43E9x//59Zfzs3r170a1bN/z888/4888/AbzpQQaQZM5dZ2dnZd27TJw4EXZ2dsqfm5tbitVMREREROpJ1rCEAQMG4MWLF+jevTvi4uIAAFZWVhg0aBCGDBmSYsXp9XqULVsWEyZMAACULl0a165dw/z589GuXbtk73fIkCHo27evshwREcGAS0RERKQByeq51el0mDRpEp49e4ZTp07h8uXLCA0NxciRI1O0uGzZsqFo0aJGbUWKFMGjR48AAC4uLgCA4OBgo22Cg4OVde9iaWkJW1tboz8iIiIiSv+SFW4NMmXKhHLlyqFYsWKwtLRMqZoUlSpVwq1bt4zabt++jVy5cgF4c3CZi4sLDhw4oKyPiIjA6dOneaY0IiIioi9QsoYlpJY+ffqgYsWKmDBhApo1a4YzZ85g4cKFWLhwIYA3Pci9e/fGuHHjUKBAAeTJkwcjRoyAq6srGjRooG7xRERERJTq0nS4LVeuHDZv3owhQ4bgl19+QZ48eTBjxgy0atVK2WbgwIGIjo7Gjz/+iLCwMFSuXBl79uyBlZWVipUTERERkRp0IiJqF6G2iIgI2NnZITw8/D/H37oPWJ5KVSXfZpspapfwQXKOvKp2CURERJROfGhe+6Qxt0REREREaQnDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMtEREREWkGwy0RERERaQbDLRERERFpBsMt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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(6,4))\n",
        "df['Sex'].value_counts().plot(kind='pie', autopct='%1.1f%%')\n",
        "plt.title(\"Gender Distribution\")\n",
        "plt.ylabel(\"\")\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 367
        },
        "id": "zg0IUKTjES6o",
        "outputId": "78cddaf3-b9fc-4d8b-e7f0-b1e1a1032b0c"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 600x400 with 1 Axes>"
            ],
            "image/png": "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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(6,4))\n",
        "sns.countplot(data=df, x='AgeGroup')\n",
        "plt.title(\"Employee Age Group Distribution\")\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 410
        },
        "id": "7IkSmMUdEZAc",
        "outputId": "346eec26-ff65-400c-989c-a9ed850dd224"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 600x400 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAAAhwAAAGJCAYAAADBveoRAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjAsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvlHJYcgAAAAlwSFlzAAAPYQAAD2EBqD+naQAAP2hJREFUeJzt3Xt8z/X///H7e6f3ZrPNmM1yDJkzOS5CrEY+4pMSkUM+SEMotM8nRLSUPjlbKuTTlI8KUUSOEWIOlRhK8aFtDm3LaWZ7/v7ou/fPu23Y7GXD7Xq5vC4X7+fz+Xq9Hq+31/a+73V4v2zGGCMAAAALuRR2AQAA4PZH4AAAAJYjcAAAAMsROAAAgOUIHAAAwHIEDgAAYDkCBwAAsByBAwAAWI7AAQAALEfgAP5iw4YNstls2rBhQ2GXgjtExYoV1bt3b8vX88svv8hms2n+/PmOtt69e8vHx8fydWex2Wx6+eWXb9r6UHQQOFCo5s+fL5vNluu0bdu2wi7xtpCRkaGQkBDZbDatXLmysMuRJH333Xfq06ePKlWqJE9PT/n4+KhevXoaOXKkfv7558IuL99atWrl2H9dXFzk6+uratWq6amnntKaNWsKbD1ffPFFkf3gLsq1ofC4FXYBgCSNHz9elSpVytZepUqVQqjm9rNu3Tr99ttvqlixomJjY9WuXbtCreedd97RwIEDVapUKXXv3l2hoaG6fPmyfvjhBy1YsEBTpkzRhQsX5OrqWqh15lfZsmUVHR0tSTp37pwOHz6sTz/9VB988IG6dOmiDz74QO7u7o7x8fHxcnHJ299/X3zxhWbOnJmnD/YKFSrowoULTuu2wtVqu3Dhgtzc+Oi5E/G/jiKhXbt2atiwYWGXcdv64IMPdO+996pXr1765z//qXPnzsnb27tQavnmm280cOBANWvWTCtWrFDx4sWd+t98801NnDjxmss5f/68ihUrZlWZN8TPz089evRwanvttdc0ZMgQzZo1SxUrVtSkSZMcfXa73dJ6Ll++rMzMTHl4eMjT09PSdV1LYa8fhYdTKrglZJ17njx5smbOnKm7775bxYoV00MPPaRjx47JGKNXXnlFZcuWlZeXlzp27KgzZ844LaNixYr629/+ptWrV6tevXry9PRUjRo19Omnn15XDYsXL1aDBg3k5eWlUqVKqUePHjp+/Lijf968ebLZbNq9e3e2eV999VW5uro6jd++fbvatm0rPz8/FStWTC1bttSWLVuyzXv8+HE9/fTTCgoKkt1uV82aNTV37tzrfet04cIFLVmyRF27dlWXLl104cIFLVu2LNdtrFGjhjw9PVWrVi0tWbJEvXv3VsWKFZ3GZWZmasqUKapZs6Y8PT0VFBSkAQMG6Pfff79mPePGjZPNZlNsbGy2sCH9+YH0yiuvOB3daNWqlWrVqqW4uDi1aNFCxYoV0z//+U9JUlJSkvr27augoCB5enqqbt26ev/9952Wmdt1OVe7puHnn39WRESEvL29FRISovHjx+tGHq7t6uqqadOmqUaNGpoxY4ZSUlIcfX+9hiM9PV3jxo1T1apV5enpqZIlS6p58+aOUzK9e/fWzJkzJcnpFOSV2zR58mRNmTJFlStXlt1u148//pjj9ma51vZe73t4tdqy2v565GP37t1q166dfH195ePjozZt2mQ7nZp1+nXLli0aPny4AgMD5e3trb///e86efLktf8DUOg4woEiISUlRadOnXJqs9lsKlmypFNbbGysLl26pMGDB+vMmTN6/fXX1aVLF7Vu3VobNmzQqFGjdPjwYU2fPl0vvPBCtg/mQ4cO6YknntAzzzyjXr16ad68eXr88ce1atUqPfjgg7nWN3/+fPXp00eNGjVSdHS0EhMTNXXqVG3ZskW7d++Wv7+/HnvsMUVGRio2Nlb169fPVnerVq101113SfrzFEe7du3UoEEDjR07Vi4uLpo3b55at26tr7/+Wo0bN5YkJSYmqmnTprLZbBo0aJACAwO1cuVK9e3bV6mpqRo6dOg139vPPvtMZ8+eVdeuXRUcHKxWrVopNjZWTz75pNO4zz//XE888YRq166t6Oho/f777+rbt6+j5isNGDDA8Z4MGTJER44c0YwZM7R7925t2bIl10P258+f17p169SqVSuVLVv2mrVf6fTp02rXrp26du2qHj16KCgoSBcuXFCrVq10+PBhDRo0SJUqVdLixYvVu3dvJScn67nnnsvTOrJkZGSobdu2atq0qV5//XWtWrVKY8eO1eXLlzV+/Ph8LVP6M3R069ZNo0eP1ubNm9W+ffscx7388suKjo7WP/7xDzVu3FipqanauXOndu3apQcffFADBgzQiRMntGbNGv3nP//JcRnz5s3TxYsX1b9/f9ntdgUEBCgzM9Py7b2e2q60b98+3X///fL19dXIkSPl7u6ut99+W61atdLGjRvVpEkTp/GDBw9WiRIlNHbsWP3yyy+aMmWKBg0apEWLFuWpThQCAxSiefPmGUk5Tna73THuyJEjRpIJDAw0ycnJjvaoqCgjydStW9ekp6c72rt162Y8PDzMxYsXHW0VKlQwkswnn3ziaEtJSTFlypQx9evXd7StX7/eSDLr1683xhhz6dIlU7p0aVOrVi1z4cIFx7gVK1YYSWbMmDFO6w0JCTEZGRmOtl27dhlJZt68ecYYYzIzM03VqlVNRESEyczMdIw7f/68qVSpknnwwQcdbX379jVlypQxp06dcnrfunbtavz8/Mz58+ev+R7/7W9/M82aNXO8njNnjnFzczNJSUlO42rXrm3Kli1r/vjjD0fbhg0bjCRToUIFR9vXX39tJJnY2Fin+VetWpVj+5X27t1rJJmhQ4dm6zt9+rQ5efKkY0pLS3P0tWzZ0kgyMTExTvNMmTLFSDIffPCBo+3SpUsmLCzM+Pj4mNTUVGNM9v/TLFn7Vdb/jTHG9OrVy0gygwcPdrRlZmaa9u3bGw8PD3Py5Mlcty+r1po1a+bav2TJEiPJTJ061dFWoUIF06tXL8frunXrmvbt2191PZGRkSanX+FZ2+Tr65vt//hGtjcv72FutRljjCQzduxYx+tOnToZDw8P89NPPznaTpw4YYoXL25atGjhaMv6XREeHu70czNs2DDj6urq9HsBRROnVFAkzJw5U2vWrHGacrqb4vHHH5efn5/jddZfPz169HC6EK1Jkya6dOmS0ykMSQoJCdHf//53x2tfX1/17NlTu3fvVkJCQo617dy5U0lJSXr22Wedzj+3b99eoaGh+vzzzx1tPXv21IkTJ7R+/XpHW2xsrLy8vNS5c2dJ0p49e3To0CE9+eSTOn36tE6dOqVTp07p3LlzatOmjTZt2qTMzEwZY/TJJ5+oQ4cOMsY4xp06dUoRERFKSUnRrl27rvq+nj59Wl9++aW6devmaOvcubNsNpv++9//OtpOnDih77//Xj179nS6RbJly5aqXbu20zIXL14sPz8/Pfjgg041NWjQQD4+Pk7b/lepqamSlONtmHfffbcCAwMd02effebUb7fb1adPH6e2L774QsHBwU7b5+7uriFDhujs2bPauHHj1d6eqxo0aJDj31lHmC5duqSvvvoq38uU/v+2//HHH7mO8ff31759+3To0KF8r6dz584KDAy87vFWbe/VZGRkaPXq1erUqZPuvvtuR3uZMmX05JNPavPmzY59Jkv//v2dTtHcf//9ysjI0K+//mpZnSgYnFJBkdC4cePrumi0fPnyTq+zwke5cuVybP/rNQVVqlRx+mUlSffcc4+kP89FBwcHZ1tn1i+yatWqZesLDQ3V5s2bHa8ffPBBlSlTRrGxsWrTpo0yMzP14YcfqmPHjo7rFbI+RHr16pXrdqakpCg9PV3JycmaM2eO5syZk+O4pKSkXJchSYsWLVJ6errq16+vw4cPO9qbNGmi2NhYRUZGOm1jTncFValSxSnYHDp0SCkpKSpdunSea8p6D86ePZutb9myZUpPT9fevXv1wgsvZOu/66675OHh4dT266+/qmrVqtnu8KhevbrTduWVi4uL0weg5Lyf3Iisbc/p+pUs48ePV8eOHXXPPfeoVq1aatu2rZ566inVqVPnuteT011fubFye6/m5MmTOn/+fI4/W9WrV1dmZqaOHTummjVrOtr/+jugRIkSkrL/rKPoIXDglpLbbZK5tZsbuMgvP1xdXfXkk0/qnXfe0axZs7RlyxadOHHC6Y6FrPPob7zxhurVq5fjcnx8fHT69GlJfx69yS2cXOsDKDY2VpLUrFmzHPt//vnnbB8015KZmanSpUs7lv1XV/urukqVKnJzc9MPP/yQra9ly5aSlOstk15eXnmq80p/DZlZMjIy8r3M/Mra9qvd8t2iRQv99NNPWrZsmVavXq13331Xb731lmJiYvSPf/zjutZzI+9XTorKe1hUftaRdwQO3FEOHz4sY4zTL8+DBw9KUrY7MbJUqFBB0p/fldC6dWunvvj4eEd/lp49e+rNN9/U8uXLtXLlSgUGBioiIsLRX7lyZUl/ns4JDw/PtdbAwEAVL15cGRkZVx2XmyNHjuibb77RoEGDHB/mWTIzM/XUU09p4cKFeumllxzbcOVRkCx/batcubK++uorNWvWLM8fat7e3o6LAY8fP57jBal5UaFCBX333XfKzMx0Ospx4MABR7/0//8KTk5Odpo/tyMgmZmZ+vnnnx1/5UvX3k+uR0ZGhhYuXKhixYqpefPmVx0bEBCgPn36qE+fPjp79qxatGihl19+2RE4cgsA+XE925uX9/B6awsM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nVJ5+umnr9o/d+7cfBXzV9988406duyo9u3bS5IqVqyoDz/8UN9++62kP49uTJkyRS+99JI6duwoSVqwYIGCgoK0dOlSde3atUDqAAAANybft8VeOSUlJWndunX69NNPlZycXGDF3XfffVq7dq0OHjwoSdq7d682b96sdu3aSfrz1E5CQoLCw8Md8/j5+alJkybaunVrrstNS0tTamqq0wQAAKyTryMcS5YsydaWmZmpgQMHqnLlyjdcVJYXX3xRqampCg0NlaurqzIyMjRx4kR1795dkpSQkCBJCgoKcpovKCjI0ZeT6OhojRs3rsDqBAAAV1dg13C4uLho+PDheuuttwpqkfrvf/+r2NhYLVy4ULt27dL777+vyZMn6/3337+h5UZFRSklJcUxHTt2rIAqBgAAOcn3w9ty8tNPP+ny5csFtrwRI0boxRdfdFyLUbt2bf3666+Kjo5Wr169FBwcLElKTExUmTJlHPMlJiaqXr16uS7XbrfLbrcXWJ0AAODq8hU4hg8f7vTaGKPffvtNn3/+uXr16lUghUnS+fPn5eLifBDG1dXV8XTaSpUqKTg4WGvXrnUEjNTUVG3fvl0DBw4ssDoAAMCNyVfg2L17t9NrFxcXBQYG6s0337zmHSx50aFDB02cOFHly5dXzZo1tXv3bv373/92rMNms2no0KGaMGGCqlatqkqVKmn06NEKCQlRp06dCqwOAABwY/IVONavX1/QdeRo+vTpGj16tJ599lklJSUpJCREAwYM0JgxYxxjRo4cqXPnzql///5KTk5W8+bNtWrVKnl6et6UGgEAwLXZzJVf25lHJ0+eVHx8vCSpWrVqCgwMLLDCbqbU1FT5+fkpJSVFvr6+eZ6/wYgFFlSFoirujZ6FXQIAFBnX+xmar7tUzp07p6efflplypRRixYt1KJFC4WEhKhv3746f/58vosGAAC3p3wFjuHDh2vjxo1avny5kpOTlZycrGXLlmnjxo16/vnnC7pGAABwi8vXNRyffPKJPv74Y7Vq1crR9vDDD8vLy0tdunTR7NmzC6o+AABwG8jXEY7z589n+3ZPSSpdujSnVAAAQDb5ChxhYWEaO3as0xNZL1y4oHHjxiksLKzAigMAALeHfJ1SmTJlitq2bauyZcuqbt26kv58sJrdbtfq1asLtEAAAHDry1fgqF27tg4dOqTY2Fgd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7du3q3Tp0rrvvvsUFBSkli1bavPmzddc1o8//qjx48drwYIFV/2LoV69eipTpowefPBBbdmypSA3B0VUZGSk2rdvr/DwcKf2G9nfspZbqlQpNW7cWHPnzs3x0djsb3emlJQUSVJAQICkG9/Xspw4cUKffvqpWrZsma2Pfe06FHbiwc333XffGW9vb+Pq6mr8/PzM559/bowxZuvWrUaSCQgIMHPnzjW7du0yQ4cONR4eHubgwYO5Lu/ixYumTp065j//+Y8xJufEf+DAARMTE2N27txptmzZYvr06WPc3NxMXFycpduKwvXhhx+aWrVqmQsXLhhjjNMRjvzub8YYM378eLN582aza9cu89prrxm73W6mTp3q6Gd/u3NlZGSY9u3bm2bNmjnabmRfM8aYrl27Gi8vLyPJdOjQwbE/G8O+lhcEjjtQWlqaOXTokNm5c6d58cUXTalSpcy+ffvMli1bjCQTFRXlNL527drmxRdfNMYY07ZtW+Pt7W28vb1NjRo1jDHGDBs2zDzxxBOO8dd7iLFFixamR48eBbtxKDKOHj1qSpcubfbu3etouzJw5Hd/y8no0aOdDnPnhP3tzvDMM8+YChUqmGPHjjnabnRf++2338z+/fvNsmXLTI0aNczAgQOvWgP7Ws64aPQO5OHhoSpVqkiSGjRooB07dmjq1Kl68cUXJUk1atRwGl+9enUdPXpUkvTuu+86rup2d3eXJK1bt07ff/+9Pv74Y0lyHNouVaqU/vWvf2ncuHE51tG4ceM8H9LErSMuLk5JSUm69957HW0ZGRnatGmTZsyY4biLIK/7W06aNGmiV155RWlpabk+B4P97fY3aNAgrVixQps2bVLZsmUd7WXKlJGU/30tODhYwcHBCg0NVUBAgO6//36NHj3asdy/Yl/LGYEDyszMVFpamipWrKiQkJBst5MdPHhQ7dq1kyTddddd2eb/5JNPnG4t27Fjh55++ml9/fXXqly5cq7r3bNnT64/sLj1tWnTRt9//71TW58+fRQaGqpRo0bp7rvvztf+lpM9e/aoRIkSV33oFvvb7csYo8GDB2vJkiXasGGDKlWq5NSf399tOcnMzJQkpaWl5TqGfS1nBI47TFRUlNq1a6fy5cvrjz/+0MKFC7VhwwZ9+eWXstlsGjFihMaOHau6deuqXr16ev/993XgwAHH0Yuc/DVUnDp1StKffz1k3ao4ZcoUVapUSTVr1tTFixf17rvvat26dVq9erVl24rCVbx4cdWqVcupzdvbWyVLlnS052d/W758uRITE9W0aVN5enpqzZo1evXVV/XCCy84xrC/3VkiIyO1cOFCLVu2TMWLF3d8B4afn5+8vLzy/bvtiy++UGJioho1aiQfHx/t27dPI0aMULNmzVSxYkVJ7Gt5UtjndHBzPf3006ZChQrGw8PDBAYGmjZt2pjVq1c7jYmOjjZly5Y1xYoVM2FhYebrr7/O0zpyuoZj0qRJpnLlysbT09MEBASYVq1amXXr1hXEJuEW8tfbYo3J+/62cuVKU69ePePj42O8vb1N3bp1TUxMjMnIyHCMYX+7s0jKcZo3b57TuLzua+vWrTNhYWHGz8/PeHp6mqpVq5pRo0bxuy2feDw9AACwHN/DAQAALEfgAAAAliNwAAAAyxE4AACA5QgcAADAcgQOAABgOQIHAACwHIEDAABYjsABAAAsR+AAcF22bt0qV1dXtW/f3rJ1HD58WE8//bTKly8vu92uu+66S23atFFsbKwuX75s2XoBWI/AAeC6vPfeexo8eLA2bdqkEydOFPjyv/32W917773av3+/Zs6cqR9++EEbNmzQP/7xD82ePVv79u3Ldd709PQCrwdAwSJwALims2fPatGiRRo4cKDat2+v+fPnO/V/9tlnqlq1qjw9PfXAAw/o/fffl81mU3JysmPM5s2bdf/998vLy0vlypXTkCFDdO7cOUl/Pl68d+/euueee7RlyxZ16NBBVatWVdWqVdWtWzdt3rxZderUkST98ssvstlsWrRokVq2bClPT0/FxsYqMzNT48ePV9myZWW321WvXj2tWrXKsf4NGzZkq2nPnj2y2Wz65ZdfJEnz58+Xv7+/li5d6tieiIgIHTt2zJL3FbiTEDgAXNN///tfhYaGqlq1aurRo4fmzp2rrOc+HjlyRI899pg6deqkvXv3asCAAfrXv/7lNP9PP/2ktm3bqnPnzvruu++0aNEibd68WYMGDZL05wf//v379cILL8jFJedfSzabzen1iy++qOeee0779+9XRESEpk6dqjfffFOTJ0/Wd999p4iICD3yyCM6dOhQnrb1/PnzmjhxohYsWKAtW7YoOTlZXbt2zdMyAOSgcB9WC+BWcN9995kpU6YYY4xJT083pUqVMuvXrzfGGDNq1ChTq1Ytp/H/+te/jCTHY7z79u1r+vfv7zTm66+/Ni4uLubChQvmo48+MpLMrl27HP2JiYnG29vbMc2cOdMYY8yRI0eMJEc9WUJCQszEiROd2ho1amSeffZZY4wx69evd6rJGGN2795tJJkjR44YY4yZN2+ekWS2bdvmGLN//34jyWzfvj0P7xiAv+IIB4Crio+P17fffqtu3bpJktzc3PTEE0/ovffec/Q3atTIaZ7GjRs7vd67d6/mz58vHx8fxxQREaHMzEwdOXIkx/WWLFlSe/bs0Z49e+Tv769Lly459Tds2NDx79TUVJ04cULNmjVzGtOsWTPt378/T9vr5ubmtD2hoaHy9/fP83IAOHMr7AIAFG3vvfeeLl++rJCQEEebMUZ2u10zZsy4rmWcPXtWAwYM0JAhQ7L1lS9fXhcuXJD0Z3ipX7++JMnV1VVVqlSR9GcI+Ctvb+88bUfWqRrzf6eCJC42BW4mjnAAyNXly5e1YMECvfnmm46jDXv27NHevXsVEhKiDz/8UNWqVdPOnTud5tuxY4fT63vvvVc//vijqlSpkm3y8PBQ/fr1FRoaqsmTJyszMzPPdfr6+iokJERbtmxxat+yZYtq1KghSQoMDJQk/fbbb47+PXv25LjNV25PfHy8kpOTVb169TzXBeAKhX1OB0DRtWTJEuPh4WGSk5Oz9Y0cOdI0bNjQ/Pzzz8bd3d2MHDnSxMfHm0WLFpmyZcsaSY759u7da7y8vExkZKTZvXu3OXjwoFm6dKmJjIx0LG/r1q3Gx8fHNG3a1CxbtswcPHjQ7Nu3z8yePdsUK1bMTJs2zRjz/6/h2L17t1M9b731lvH19TUfffSROXDggBk1apRxd3c3Bw8eNMYYc+nSJVOuXDnz+OOPm4MHD5oVK1aYatWqZbuGw93d3TRu3Nhs27bN7Ny50zRt2tQ0bdrUgncXuLMQOADk6m9/+5t5+OGHc+zbvn27kWT27t1rli1bZqpUqWLsdrtp1aqVmT17tpFkLly44Bj/7bffmgcffND4+PgYb29vU6dOnWwXecbHx5tevXqZsmXLGjc3N+Pn52datGhh3n77bZOenm6MyT1wZGRkmJdfftncddddxt3d3dStW9esXLnSaczmzZtN7dq1jaenp7n//vvN4sWLswUOPz8/88knn5i7777b2O12Ex4ebn799dcbfCcB2Iy54oQmABSAiRMnKiYm5pb7/or58+dr6NChTt/VAaBgcNEogBs2a9YsNWrUSCVLltSWLVv0xhtvOL5jAwAkAgeAAnDo0CFNmDBBZ86cUfny5fX8888rKiqqsMsCUIRwSgUAAFiO22IBAIDlCBwAAMByBA4AAGA5AgcAALAcgQMAAFiOwAEAACxH4AAAAJYjcAAAAMv9PyytrJR2HIIZAAAAAElFTkSuQmCC\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(7,5))\n",
        "sns.boxplot(data=df, x='PerformanceScore', y='Salary')\n",
        "plt.title(\"Salary vs Performance Score\")\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 487
        },
        "id": "8p34oLmPEmZI",
        "outputId": "54f97b6d-febb-44da-a36d-0089cb4a556e"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 700x500 with 1 Axes>"
            ],
            "image/png": "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TZvwxx9/SOcWBgQEIC4uDjExMbCxscE777wDADhy5Eix3m92djZsbW2RlZXFvYVERYiPj0dUVJTBeblOTk4ICAiAt7e3ESsjIqp6SpQ7ynvK87MAKPKxdu1aIYQQaWlpwtvbW9jb2wuVSiWaNGkiZs2aVWj69KVLl0SfPn2EhYWFqFOnjpgxY4bIz883GLN//37Rrl07YWZmJtzd3aV1PG7lypXCxcVFmJmZic6dO4ujR48a9D98+FAEBgaKWrVqCUtLSzFw4ECRnp5e7PfLy84QPV9BQYE4deqU+OWXX8SpU6d4qRkiolIqSe4w6h5CueEeQiIiIqooJckdlWJSCREREREZDwMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJHAMhERERkcwxEBIRERHJXA1jF0DypNVqodFokJmZCXt7e3h6ekKpVBq7LCIiIlliIKQKFx8fj6ioKGRkZEhtjo6OCAwMhLe3txErIyIikiceMqYKFR8fj7CwMLi7uyMyMhJxcXGIjIyEu7s7wsLCEB8fb+wSiYiIZMdECCGMXYRcZGdnw9bWFllZWbCxsTF2ORVOq9VCrVbD3d0dERERUCj+9/eITqdDaGgoUlNTsX79eh4+JiIi+pdKkju4h5AqjEajQUZGBtRqtUEYBACFQgG1Wo309HRoNBojVUhERCRPDIRUYTIzMwEAbm5uRfbr2/XjiIiIqGIwEFKFsbe3BwCkpqYW2a9v148jIiKiisFASBXG09MTjo6OiI2NhU6nM+jT6XSIjY2Fk5MTPD09jVQhERGRPDEQUoVRKpUIDAxEQkICQkNDkZSUhJycHCQlJSE0NBQJCQkICAjghBIiIqIKxlnGFUjus4z1iroOoZOT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\n"
          },
          "metadata": {}
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "plt.figure(figsize=(7,5))\n",
        "sns.boxplot(data=df, x='Attrition', y='Absences')\n",
        "plt.title(\"Absence Impact on Attrition\")\n",
        "plt.show()"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 487
        },
        "id": "HtrB5MCmEvv-",
        "outputId": "9807053c-2196-4463-e59f-6e27b0cb25e9"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "display_data",
          "data": {
            "text/plain": [
              "<Figure size 700x500 with 1 Axes>"
            ],
            "image/png": "iVBORw0KGgoAAAANSUhEUgAAAm4AAAHWCAYAAADO2QWWAAAAOnRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjEwLjAsIGh0dHBzOi8vbWF0cGxvdGxpYi5vcmcvlHJYcgAAAAlwSFlzAAAPYQAAD2EBqD+naQAAPSRJREFUeJzt3XlclOX+//H3CDIQ4qiJLImgmJK7WZFbbiSSWZa5PSqXLDsdzUyrE6fOcWnxZJsZSptKpqUtii2mmbmc0jL1UGplaij6TTBNQUhB5fr94Y/JiUVGB4ZbX8/H437Ufd3Xfd2f+y6GN/c2NmOMEQAAAKq8at4uAAAAAOVDcAMAALAIghsAAIBFENwAAAAsguAGAABgEQQ3AAAAiyC4AQAAWATBDQAAwCIIbgAAABZBcAMsZvfu3bLZbHruuee8XQpQIaKiojRs2LBy9e3atau6du1aofUAVQnBDahiZs6cKZvNptjYWG+XUmWlpKTIZrNp48aN3i7lvC1dulQTJ070dhmlOnXqlMLDw2Wz2fTpp5+W2GfmzJlKSUkp1v7DDz9o4sSJ2r1793nV4KlxgAsBwQ2oYubPn6+oqCht2LBBO3fu9HY5qGBLly7VpEmTvF1Gqb744gvt379fUVFRmj9/fol9ygpukyZNcjtwbd++Xa+//nq5xvnss8/02WefuTU+YGUEN6AKSU9P17p16/TCCy8oODi41F+UQGWZN2+errzySj344INKTU1VXl5ehWzHGKNjx45Jkux2u6pXr16u9fz8/OTn51chNQFVEcENqELmz5+v2rVrq3fv3rrtttvOGtxefPFFRUZGKiAgQF26dNHWrVtdlmdmZmr48OGqX7++7Ha7wsLCdPPNNxc7c/Hpp5+qc+fOCgwMVFBQkHr37q1t27a59Bk2bJhq1Kih//u//1Pfvn1Vo0YNBQcH66GHHtKpU6dc+hYWFuqll15Sy5Yt5e/vr+DgYPXq1avYpc158+apXbt2CggIUJ06dTRo0CDt3bvXzaPmWl9GRoZuvPFG1ahRQ5dddplmzJghSdqyZYu6d++uwMBARUZG6u2333ZZv+jy69q1a3Xvvffq0ksvVc2aNTVkyBAdPnzYpe+SJUvUu3dvhYeHy263Kzo6Wk888USx4yBJ33zzjW644QbVrl1bgYGBatWqlV566SVnzUX12Ww253Q2M2fOVPPmzWW32xUeHq5Ro0bpyJEjLn26du2qFi1a6IcfflC3bt10ySWX6LLLLtPUqVPLfUyPHTumxYsXa9CgQRowYICOHTumJUuWuPSJiorStm3btGbNGmf9Xbt2VUpKivr37y9J6tatm3PZ6tWrnevdeOONWr58ua666ioFBATo1VdfdS4rusftbOOUdI/bgQMHNGLECIWEhMjf31+tW7fWm2++6dLnzHtFX3vtNUVHR8tut+vqq6/Wt99+W+5jBFQ6A6DKiImJMSNGjDDGGLN27VojyWzYsMGlT3p6upFkWrZsaaKioswzzzxjJk2aZOrUqWOCg4NNZmams2+HDh2Mw+Ewjz/+uHnjjTfM008/bbp162bWrFnj7DN37lxjs9lMr169zMsvv2yeeeYZExUVZWrVqmXS09Od/YYOHWr8/f1N8+bNzV133WWSk5NNv379jCQzc+ZMlxqHDRtmJJmEhAQzbdo089xzz5mbb77ZvPzyy84+Tz75pLHZbGbgwIFm5syZZtKkSaZu3bomKirKHD58uMzjNGfOHCPJfPvtt8Xqa9asmfnb3/5mZsyYYTp06GAkmTlz5pjw8HDz8MMPm5dfftk0b97c+Pj4mF9++aXYmC1btjSdO3c206dPN6NGjTLVqlUz1113nSksLHT27du3rxkwYIB59tlnTXJysunfv7+RZB566CGXOj/77DPj5+dnIiMjzYQJE0xycrIZM2aMiYuLM8YYs27dOnP99dcbSeatt95yTmWZMGGCkWTi4uLMyy+/bEaPHm18fHzM1VdfbQoKCpz9unTpYsLDw01ERIR54IEHzMyZM0337t2NJLN06dIyt1FkwYIFxmazmYyMDGOMMd27dzc33HCDS5/Fixeb+vXrm5iYGGf9n332mdm1a5cZM2aMkWT++c9/OpcV/f8ZGRlpGjdubGrXrm0effRR88orr5hVq1Y5lw0dOtQYY846TpcuXUyXLl2c9fzxxx/miiuuMNWrVzcPPvigmT59uuncubORZKZNm+bsV/Rz1LZtW9O4cWPzzDPPmKlTp5q6deua+vXruxxLoCohuAFVxMaNG40ks2LFCmOMMYWFhaZ+/frmgQcecOlX9AsnICDA7Nu3z9n+zTffGEnmwQcfNMYYc/jwYSPJPPvss6Vu8+jRo6ZWrVrmnnvucWnPzMw0DofDpX3o0KFGkpk8ebJL37Zt25p27do557/44gsjyYwZM6bY9orCz+7du42Pj4956qmnXJZv2bLF+Pr6Fmv/q9KCmyTz9NNPO9sOHz5sAgICjM1mMwsWLHC2//TTT0aSmTBhQrEx27Vr5/JLe+rUqUaSWbJkibPtjz/+KFbTvffeay655BJz/PhxY4wxJ0+eNA0bNjSRkZHFguiZIXDUqFGmvH9DHzhwwPj5+ZmePXuaU6dOOduTkpKMJDN79mxnW5cuXYwkM3fuXGdbfn6+CQ0NNf369SvX9m688UbTsWNH5/xrr71mfH19zYEDB1z6NW/e3CU8FXnvvfeMJGcgO1NkZKSRZJYtW1bisqLgdrZx/hrcpk2bZiSZefPmOdsKCgpM+/btTY0aNUxOTo4x5s+fo0svvdT8/vvvzr5LliwxksxHH31UbFtAVcClUqCKmD9/vkJCQtStWzdJpy+dDRw4UAsWLCjxElzfvn112WWXOeevueYaxcbGaunSpZKkgIAA+fn5afXq1cUu9RVZsWKFjhw5osGDB+vgwYPOycfHR7GxsVq1alWxdf72t7+5zHfu3Fm//PKLc/6DDz6QzWbThAkTiq1bdBlw0aJFKiws1IABA1y2Gxoaqssvv7zE7ZbX3Xff7fz3WrVqqWnTpgoMDNSAAQOc7U2bNlWtWrVc6i4ycuRIl/ur7rvvPvn6+jqPq3T62BY5evSoDh48qM6dO+uPP/7QTz/9JEn63//+p/T0dI0dO1a1atUq8Ti46/PPP1dBQYHGjh2ratX+/Pi+5557VLNmTX3yyScu/WvUqKE77rjDOe/n56drrrmmxP3+q0OHDmn58uUaPHiws61fv36y2Wx69913z6n+v2rYsKHi4+M9MlaRpUuXKjQ01KXu6tWra8yYMcrNzdWaNWtc+g8cOFC1a9d2znfu3FmSynWMAG/w9XYBAE6/cmHBggXq1q2b0tPTne2xsbF6/vnntXLlSvXs2dNlncsvv7zYOE2aNHH+UrXb7XrmmWc0fvx4hYSE6Nprr9WNN96oIUOGKDQ0VJK0Y8cOSVL37t1LrKtmzZou80X3q52pdu3aLsFw165dCg8PV506dUrd3x07dsgYU+I+SCr3jel/VVJ9DodD9evXLxaWHA5HiYH2rzXVqFFDYWFhLvcFbtu2TY8//ri++OIL5eTkuPTPzs6WdPo4SFKLFi3OaV9KsmfPHkmng+eZ/Pz81KhRI+fyIiXtd+3atfX999+fdVsLFy7UiRMn1LZtW5enm2NjYzV//nyNGjXqXHfDqWHDhuc9xl/t2bNHl19+uUuwlaQrrrjCufxMDRo0cJkvCnGl/bEDeBvBDagCil65sGDBAi1YsKDY8vnz5xcLbuUxduxY9enTR6mpqVq+fLn+9a9/acqUKfriiy/Utm1bFRYWSpLeeustZ5g7k6+v60eEj4+P2zWUpLCw0PlesJLGrFGjxjmNW1p9pbUbY9zexpEjR9SlSxfVrFlTkydPVnR0tPz9/bV582b94x//cB7TquB89rvowZiOHTuWuPyXX35Ro0aNzr04uZ659BZP/r8BVAaCG1AFzJ8/X/Xq1XM+YXimRYsWafHixXrllVdcftEVnS07088//6yoqCiXtujoaI0fP17jx4/Xjh071KZNGz3//POaN2+eoqOjJUn16tVTXFycR/YlOjpay5cv1++//17qWbfo6GgZY9SwYUM1adLEI9v1lB07djgvV0tSbm6u9u/frxtuuEGStHr1ah06dEiLFi3Sdddd5+x35plSSc5ju3Xr1jKPrTuXTSMjIyWdfs/ZmaGpoKBA6enpHvtvWPRamtGjR6tLly4uywoLC3XnnXfq7bff1uOPPy6p9H0410vC5zNOZGSkvv/+exUWFrqcdSu6hF10DAGr4h43wMuOHTumRYsW6cYbb9Rtt91WbBo9erSOHj2qDz/80GW91NRU/d///Z9zfsOGDfrmm2+UkJAgSfrjjz90/Phxl3Wio6MVFBSk/Px8SVJ8fLxq1qypp59+WidOnChW22+//eb2/vTr10/GmBJfKlt0FuPWW2+Vj4+PJk2aVOzMhjFGhw4dcnu7nvLaa6+5HIvk5GSdPHnSeVyLztCcWXdBQYFmzpzpMs6VV16phg0batq0acVe1XHmuoGBgZJUrE9J4uLi5Ofnp+nTp7uMMWvWLGVnZ6t3797l28mzKDrb9sgjjxT7/3HAgAHq0qWLy6tqAgMDS6zfnX0rizvj3HDDDcrMzNTChQudbSdPntTLL7+sGjVqFAuigNVwxg3wsg8//FBHjx7VTTfdVOLya6+91vky3oEDBzrbGzdurE6dOum+++5Tfn6+pk2bpksvvVSPPPKIpNNn33r06KEBAwaoWbNm8vX11eLFi5WVlaVBgwZJOn0PW3Jysu68805deeWVGjRokIKDg5WRkaFPPvlEHTt2VFJSklv7061bN915552aPn26duzYoV69eqmwsFD//e9/1a1bN40ePVrR0dF68sknlZiYqN27d6tv374KCgpSenq6Fi9erJEjR+qhhx46xyN6fgoKCpzHbfv27Zo5c6Y6derk/O/ToUMH1a5dW0OHDtWYMWNks9n01ltvFQug1apVU3Jysvr06aM2bdpo+PDhCgsL008//aRt27Zp+fLlkqR27dpJksaMGaP4+Hj5+Pg4//v8VXBwsBITEzVp0iT16tVLN910k7PGq6++2uVBhPMxf/58tWnTRhERESUuv+mmm3T//fdr8+bNuvLKK9WuXTslJyfrySefVOPGjVWvXj11795dbdq0kY+Pj5555hllZ2fLbrere/fuqlevnlv1uDPOyJEj9eqrr2rYsGHatGmToqKi9P777+urr77StGnTFBQUdE7HBKgyvPIsKwCnPn36GH9/f5OXl1dqn2HDhpnq1aubgwcPOl9j8Oyzz5rnn3/eREREGLvdbjp37my+++475zoHDx40o0aNMjExMSYwMNA4HA4TGxtr3n333WLjr1q1ysTHxxuHw2H8/f1NdHS0GTZsmNm4caOzz9ChQ01gYGCxdYveK3amkydPmmeffdbExMQYPz8/ExwcbBISEsymTZtc+n3wwQemU6dOJjAw0AQGBpqYmBgzatQos3379jKPWWmvAympvi5dupjmzZsXa4+MjDS9e/cuNuaaNWvMyJEjTe3atU2NGjXM7bffbg4dOuSy7ldffWWuvfZaExAQYMLDw80jjzxili9fXuIrK7788ktz/fXXm6CgIBMYGGhatWrl8j67kydPmvvvv98EBwcbm81WrleDJCUlmZiYGFO9enUTEhJi7rvvvmKvHCltv4cOHWoiIyNLHXvTpk1GkvnXv/5Vap/du3e7vHomMzPT9O7d2wQFBRlJLq/neP31102jRo2Mj4+Py/H56/E/019fB1LWOH99HYgxxmRlZZnhw4ebunXrGj8/P9OyZUszZ84clz5n/hz9lf7yqhigKrEZwx2YAJCSkqLhw4fr22+/1VVXXeXtcgCgRNzjBgAAYBEENwAAAIsguAEAAFgE97gBAABYBGfcAAAALILgBgAAYBG8gLcEhYWF+vXXXxUUFOSxr2wBAAAojTFGR48eVXh4uMvXtf0Vwa0E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zp07SwxudevWlY+Pj7Kyslzas7KyyrxPzm63y263e7xedxT6O1QYWNerNQAAgKrNUu9x27dvnw4dOqSwsLASl/v5+aldu3ZauXKls62wsFArV65U+/btK6tMAACACuHV4Jabm6u0tDSlpaVJktLT05WWlqaMjAzl5ubq4Ycf1tdff63du3dr5cqVuvnmm9W4cWPFx8c7x+jRo4eSkpKc8+PGjdPrr7+uN998Uz/++KPuu+8+5eXlOZ8yBQAAsCqvXirduHGjunXr5pwvus9s6NChSk5O1vfff68333xTR44cUXh4uHr27KknnnjC5bLmrl27dPDgQef8wIED9dtvv+nf//63MjMz1aZNGy1btox7WwAAgOV5Nbh17dpVxphSly9fvvysY+zevbtY2+jRozV69OjzKQ0AAKDKsdQ9bgAAABczghsAAIBFENwAAAAsguAGAABgEQQ3AAAAiyC4AQAAWATBDQAAwCIIbgAAABZBcAMAALAIghsAAIBFENwAAAAsguAGAABgEQQ3AAAAiyC4AQAAWATBDQAAwCIIbgAAABZBcAMAALAIghsAAIBFENwAAAAsguAGAABgEQQ3AAAAiyC4AQAAWATBDQAAwCIIbgAAABZBcAMAALAIghsAAIBFENwAAAAsguAGAABgEQQ3AAAAiyC4AQAAWATBDQAAwCIIbgAAABZBcAMAALAIghsAAIBFENwAAAAswqvBbe3aterTp4/Cw8Nls9mUmprqXHbixAn94x//UMuWLRUYGKjw8HANGTJEv/76a5ljTpw4UTabzWWKiYmp4D0BAACoeF4Nbnl5eWrdurVmzJhRbNkff/yhzZs361//+pc2b96sRYsWafv27brpppvOOm7z5s21f/9+5/Tll19WRPkAAACVytebG09ISFBCQkKJyxwOh1asWOHSlpSUpGuuuUYZGRlq0KBBqeP6+voqNDTUo7UCAAB4m6XuccvOzpbNZlOtWrXK7Ldjxw6Fh4erUaNGuv3225WRkVFm//z8fOXk5LhMAAAAVY1lgtvx48f1j3/8Q4MHD1bNmjVL7RcbG6uUlBQtW7ZMycnJSk9PV+fOnXX06NFS15kyZYocDodzioiIqIhdAAAAOC+WCG4nTpzQgAEDZIxRcnJymX0TEhLUv39/tWrVSvHx8Vq6dKmOHDmid999t9R1EhMTlZ2d7Zz27t3r6V0AAAA4b169x608ikLbnj179MUXX5R5tq0ktWrVUpMmTbRz585S+9jtdtnt9vMtFQAAoEJV6TNuRaFtx44d+vzzz3XppZe6PUZubq527dqlsLCwCqgQAACg8ng1uOXm5iotLU1paWmSpPT0dKWlpSkjI0MnTpzQbbfdpo0bN2r+/Pk6deqUMjMzlZmZqYKCAucYPXr0UFJSknP+oYce0po1a7R7926tW7dOt9xyi3x8fDR48ODK3j0AAACP8uql0o0bN6pbt27O+XHjxkmShg4dqokTJ+rDDz+UJLVp08ZlvVWrVqlr166SpF27dungwYPOZfv27dPgwYN16NAhBQcHq1OnTvr6668VHBxcsTsDAABQwbwa3Lp27SpjTKnLy1pWZPfu3S7zCxYsON+yAAAAqqTzvlSak5Oj1NRU/fjjj56oBwAAAKVwO7gNGDDAeU/ZsWPHdNVVV2nAgAFq1aqVPvjgA48XCAAAgNPcDm5r165V586dJUmLFy+WMUZHjhzR9OnT9eSTT3q8QAAAAJzmdnDLzs5WnTp1JEnLli1Tv379dMkll6h3797asWOHxwsEAADAaW4Ht4iICK1fv155eXlatmyZevbsKUk6fPiw/P39PV4gAAAATnP7qdKxY8fq9ttvV40aNdSgQQPnaznWrl2rli1bero+AAAA/H9uB7e///3vuuaaa7R3715df/31qlbt9Em7Ro0acY8bAABABTqn97hdddVVatWqldLT0xUdHS1fX1/17t3b07UBAADgDG7f4/bHH39oxIgRuuSSS9S8eXNlZGRIku6//3795z//8XiBAAAAOM3t4JaYmKjvvvtOq1evdnkYIS4uTgsXLvRocQAAAPiT25dKU1NTtXDhQl177bWy2WzO9ubNm2vXrl0eLQ4AAAB/cvuM22+//aZ69eoVa8/Ly3MJcgAAAPAst4PbVVddpU8++cQ5XxTW3njjDbVv395zlQEAAMCF25dKn376aSUkJOiHH37QyZMn9dJLL+mHH37QunXrtGbNmoqoEQAAADqHM26dOnVSWlqaTp48qZYtW+qzzz5TvXr1tH79erVr164iagQAAIDO8T1u0dHRev311z1dCwAAAMrg9hm3pUuXavny5cXaly9frk8//dQjRQEAAKA4t4Pbo48+qlOnThVrN8bo0Ucf9UhRAAAAKM7t4LZjxw41a9as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nnmmousFAAC4aJXrUmmtWrVks9mc88YYDRgwwNlW9C62Pn366NSpUxVQJgAAAMoV3FatWlWuwbZs2XJexQAAAKB05QpuXbp0KXXZ0aNH9c477+iNN97Qpk2b+MYCAACACuL2wwlF1q5dq6FDhyosLEzPPfecunfvrq+//tqTtQEAAOAMbr0OJDMzUykpKZo1a5ZycnI0YMAA5efnKzU1Vc2aNauoGgEAACA3zrj16dNHTZs21ffff69p06bp119/1csvv1yRtQEAAOAM5T7j9umnn2rMmDG67777dPnll1dkTQAAAChBuc+4ffnllzp69KjatWun2NhYJSUl6eDBgxVZGwAAAM5Q7uB27bXX6vXXX9f+/ft17733asGCBQoPD1dhYaFWrFiho0ePVmSdAAAAFz23nyoNDAzUXXfdpS+//FJbtmzR+PHj9Z///Ef16tXTTTfdVBE1AgAAQOfxOhBJatq0qaZOnap9+/bpnXfe8VRNAAAAKMF5BbciPj4+6tu3rz788ENPDAcAAIASeCS4AQAAoOIR3AAAACyC4AYAAGARBDcAAACLILgBAABYBMENAADAIghuAAAAFkFwAwAAsAiCGwAAgEUQ3AAAACyC4AYAAGARBDcAAACLILgBAABYBMENAADAIghuAAAAFkFwAwAAsIgqH9yioqJks9mKTaNGjSqxf0pKSrG+/v7+lVw1AACA5/l6u4Cz+fbbb3Xq1Cnn/NatW3X99derf//+pa5Ts2ZNbd++3Tlvs9kqtEYAAIDKUOWDW3BwsMv8f/7zH0VHR6tLly6lrmOz2RQaGlrubeTn5ys/P985n5OT436hAAAAFazKXyo9U0FBgebNm6e77rqrzLNoubm5ioyMVEREhG6++WZt27atzHGnTJkih8PhnCIiIjxdOgAAwHmzVHBLTU3VkSNHNGzYsFL7NG3aVLNnz9aSJUs0b948FRYWqkOHDtq3b1+p6yQmJio7O9s57d27twKqBwAAOD9V/lLpmWbNmqWEhASFh4eX2qd9+/Zq3769c75Dhw664oor9Oqrr+qJJ54ocR273S673e7xegEAADzJMsFtz549+vzzz7Vo0SK31qtevbratm2rnTt3VlBlAAAAlcMyl0rnzJmjevXqqXfv3m6td+rUKW3ZskVhYWEVVBkAAEDlsERwKyws1Jw5czR06FD5+rqeJBwyZIgSExOd85MnT9Znn32mX375RZs3b9Ydd9yhPXv26O67767ssgEAADzKEpdKP//8c2VkZOiuu+4qtiwjI0PVqv2ZPw8fPqx77rlHmZmZql27ttq1a6d169apWbNmlVkyAACAx1kiuPXs2VPGmBKXrV692mX+xRdf1IsvvlgJVQEAAFQuS1wqBQAAAMENAADAMghuAAAAFkFwAwAAsAiCGwAAgEUQ3AAAACyC4AYAAGARBDcAAACLILgBAABYBMENAADAIghuAAAAFkFwAwAAsAiCGwAAgEUQ3AAAACyC4AYAAGARBDcAAACLILgBAABYBMENAADAIghuAAAAFuHr7QIAAOeu2vFsb5cAXJCq6s8WwQ0ALMjhcKi6n136ZY23SwEuWNX97HI4HN4uwwXBDQAsKCQkRPPemqvs7Kp5VgDF7dmzR0899ZQee+wxRUZGersclIPD4VBISIi3y3BBcAMAiwoJCalyv1RwdpGRkWrSpIm3y4BF8XACAACARRDcAAAALILgBgAAYBEENwAAAIsguAEAAFgEwQ0AAMAiCG4AAAAWQXADAACwCIIbAACARRDcAAAALILgBgAAYBEENwAAAIuo0sFt4sSJstlsLlNMTEyZ67z33nuKiYmRv7+/WrZsqaVLl1ZStQAAABWrSgc3SWrevLn279/vnL788stS+65bt06DBw/WiBEj9L///U99+/ZV3759tXXr1kqsGAAAoGJU+eDm6+ur0NBQ51S3bt1S+7700kvq1auXHn74YV1xxRV64okndOWVVyopKakSKwYAAKgYVT647dixQ+Hh4WrUqJFuv/12ZWRklNp3/fr1iouLc2mLj4/X+vXry9xGfn6+cnJyXCYAAICqpkoHt9jYWKWkpGjZsmVKTk5Wenq6OnfurKNHj5bYPzMzUyEhIS5tISEhyszMLHM7U6ZMkcPhcE4REREe2wcAAABPqdLBLSEhQf3791erVq0UHx+vpUuX6siRI3r33Xc9up3ExERlZ2c7p71793p0fAAAAE/w9XYB7qhVq5aaNGminTt3lrg8NDRUWVlZLm1ZWVkKDQ0tc1y73S673e6xOgEAACpClT7j9le5ubnatWuXwsLCSlzevn17rVy50qVtxYoVat++fWWUBwAAUKGqdHB76KGHtGbNGu3evVvr1q3TLbfcIh8fHw0ePFiSNGTIECUmJjr7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\n"
          },
          "metadata": {}
        }
      ]
    }
  ]
}
